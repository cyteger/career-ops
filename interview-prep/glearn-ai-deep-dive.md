# GLearn — AI Technical Deep Dive

**Companion to:** [glearn-ai-software-engineer.md](glearn-ai-software-engineer.md)
**Purpose:** Sharpen the AI-specific answers. Practitioner-to-practitioner depth.

The bar in this round is not "do you know what RAG is." The bar is "have you made tradeoffs in production." Frame every answer around a decision you made and what you'd do differently.

---

## 1. Walk me through an agent you've built

This is the most likely opener. Have one agent ready with crisp specifics. Don't list three at once. Pick the strongest and go deep.

**Recommended: the sysadmin agent.** It's the riskiest (touches production) which makes the trust-boundary discussion natural, which is exactly what the GLearn JD signals they care about ("review rigorously").

### The 4-part structure

1. **Job:** "It runs controlled operations against my Linux production servers — restart services, check logs, rotate keys, generate diagnostic reports."
2. **Architecture:** "Claude API with tool-use. The tools wrap server commands as typed functions: `restart_service(name)`, `tail_logs(service, lines)`, `check_disk_usage(mount)`. Each tool has a JSON schema for inputs and a Pydantic model for the structured output it returns."
3. **Trust boundary:** "Every write operation hits an HITL approval gate before it executes. Read operations are unrestricted. The gate is a CLI prompt today; in production it would be a Slack approval flow with the proposed command, the agent's reasoning, and an expiration timer."
4. **Failure modes I designed for:**
   - **Hallucinated tool args** — Pydantic validates inputs before the command runs. Invalid args bounce back to the agent as an error tool-result, the agent re-tries with corrected args.
   - **Infinite tool loops** — hard cap on tool calls per session (10), plus a circuit breaker that detects repeated identical calls.
   - **Cost runaway** — token budget per session, monitored via the `usage` block in API responses.
   - **Prompt drift** — system prompts are versioned in git, with a small eval suite of canonical scenarios (5-10) that I run before promoting a new prompt.

### If they ask "how is this different from a shell script?"

The answer is *judgment under ambiguity*. A script does exactly what you tell it. An agent decides which tool to use, in what order, when to ask for confirmation, when to give up. That's only valuable when the input space is too messy for a script — log triage with novel error patterns, multi-step diagnostics that depend on intermediate findings.

### If they ask "what would you change about your architecture?"

Honest answer wins. Pick one:
- "I'd add explicit eval gates between tool calls — right now the agent self-evaluates whether the previous tool call worked. A separate critic model would catch more errors."
- "I'd move from a single agent with all tools to a router + specialists — too many tools in one prompt degrades selection quality past about 15 tools."

---

## 2. Prompt engineering — what works in production

If they ask "how do you write production prompts," do not say "I write clear prompts and iterate." Be specific.

### The five techniques you actually use

1. **Structured output as a contract.** Every prompt that produces data uses a JSON schema (Anthropic's `tool_use` mechanism, OpenAI's `response_format`, or strict JSON via examples). The schema is the contract; the prompt is just the instruction to satisfy it.
2. **Few-shot for format, instructions for behavior.** Examples teach output shape. Instructions teach what to do. Mixing them muddies the signal — keep them separate sections.
3. **Chain-of-thought before structured output.** For grading-like tasks, ask the model to reason in a `<thinking>` block before emitting the final JSON. The reasoning is for the model, not the user. You strip it before display.
4. **Explicit refusal paths.** Production prompts must include "if you cannot determine X, return `{result: null, reason: '...'}`". Otherwise models hallucinate confident garbage.
5. **Versioning + evals.** Prompts live in git as files (not strings in code). Each prompt has a paired eval file with 5-20 input/expected-output pairs. CI runs the evals on prompt changes.

### Anti-patterns you've stopped doing

- "You are a helpful assistant" boilerplate. Adds nothing, costs tokens.
- Negotiation language ("please", "if possible"). Direct imperatives work better.
- Putting examples after instructions. Examples-first primes the model better.
- Using temperature > 0 for structured tasks. Determinism matters more than creativity for grading and tool-use.

---

## 3. AI grading system design — the product question

This is the most likely system design prompt. **Practice it aloud once before the interview.** Here's the answer shape.

### Problem framing

WAEC has multiple answer types. The grading approach changes per type:

| Answer type | Grading approach |
|-------------|------------------|
| Multiple choice | Exact match. No LLM needed. |
| Short answer (1-2 sentences) | LLM with rubric and exemplars. Structured output: correct/partial/incorrect + feedback. |
| Free-text essay | LLM with multi-criterion rubric. Output: per-criterion score + overall + feedback. Optional second-pass critic. |
| Math (working shown) | Symbolic checker + LLM for partial credit on method. |

**Lead with this taxonomy.** It shows you understand that "AI grading" is not one problem.

### Architecture for short-answer grading

```
Student answer
  ↓
Pre-filter (length, language, banned content) — cheap, no LLM
  ↓
Cache lookup (hash of question_id + normalized_answer) — saves cost on repeat answers
  ↓
LLM grader (Claude Haiku for routine, Sonnet for ambiguous)
  Inputs: question, rubric, exemplars (3-5), student answer
  Output: { score: 0-1, breakdown: {...}, feedback: string, confidence: 0-1 }
  ↓
Confidence check
  If confidence < threshold → escalate to Sonnet/Opus or human review queue
  ↓
Store grade + write back to mastery model
```

### Cost math (have this number ready)

For Claude Haiku at roughly $0.25 / M input + $1.25 / M output tokens. A typical short-answer grading prompt is ~1500 input + ~200 output tokens.

- Per grade: ~$0.0006
- 5M students × 50 questions/week × 4 weeks = 1B grades/month → $600K/month *if you grade every answer with an LLM*

**That number is too big.** This is where you show senior judgement:

1. Cache hashable answers (multiple choice doesn't even hit LLM, factual short answers cache hit ~30-60%).
2. Use cheaper model by default, escalate by confidence.
3. Batch non-urgent grading (overnight runs at lower priority).
4. Anthropic prompt caching for the rubric+exemplars (the question changes, the rubric is stable). Cache hit drops input cost by ~90%.
5. Distill: use Sonnet to grade a sample, fine-tune a smaller model on those grades for the long tail.

If they ask "what's the realistic per-grade cost?" — say "$0.0001 to $0.0005 with caching and tiered models, possibly lower with distillation."

### What goes wrong

- **Bias against non-standard English.** WAEC essays are written by students whose first language often isn't English. Models penalize "non-standard" phrasing. Mitigation: rubric explicitly weights ideas over grammar, plus a calibration set with known-good answers across dialect ranges.
- **Reward hacking.** Students figure out the model likes certain phrases. Mitigation: rotate exemplars, periodically audit grade distributions for sudden shifts.
- **Drift between graders and humans.** Run a weekly sample where humans regrade 0.5% and you measure agreement.

---

## 4. Adaptive learning — design question

If they push into product, this is the second-likely prompt: "design the adaptive question selection."

### Core data model

```
Topic (subject, name, prerequisites: [Topic])
Question (topic, difficulty 1-5, type, content, answer_key, rubric_id)
Mastery (student, topic, score 0-1, last_practiced_at, decay_rate)
Attempt (student, question, answer, grade, time_spent, attempted_at)
```

### Selection algorithm (start simple)

1. Compute *effective mastery* per topic = `mastery_score * exp(-decay_rate * days_since_practiced)`.
2. Find topics where effective mastery is in the *learning zone* (0.4-0.8 — too high is boring, too low is frustrating).
3. Within those topics, weight by curriculum priority (WAEC syllabus weight) and prerequisite gates (don't surface a topic whose prereqs are below 0.5).
4. Pick a question of difficulty matching the student's current mastery in that topic (mastery 0.5 → question difficulty 3 of 5).
5. Apply spacing — don't surface the same question within N days unless it was answered wrong.

This is *not* a spaced-repetition flashcard system (Anki/SM-2). It's closer to a *Bayesian Knowledge Tracing* or *Elo-rating-style* system. Have those words ready if they push on the algorithm.

### When to reach for ML vs. rules

Start with rules (above). Move to ML only when you have enough attempt data to train. The first ML model is usually IRT (Item Response Theory) — every question gets a difficulty parameter, every student gets an ability parameter, both are inferred from attempts. That's what Khan Academy and Duolingo do under the hood.

### What an LLM adds here

Not the selection itself. The selection is a math problem. The LLM adds:
- **Adaptive hints** when the student is stuck.
- **Personalized explanations** of why an answer is wrong.
- **Generated practice questions** in the student's weak areas (with human review before they go live).

---

## 5. RAG — when and how

If they ask about RAG (likely, because the JD mentions structured-content workflows):

### When you reach for it

Not for grading short answers (rubric fits in context). Yes for:
- Tutoring chatbot that needs syllabus-grounded answers
- Generating practice questions from textbook chapters
- Answering "explain this topic in WAEC's terms" with citations

### Stack you'd reach for

- **Embeddings:** OpenAI `text-embedding-3-small` or Voyage. Don't overthink this.
- **Vector store:** Supabase pgvector (since they're on Supabase). One less moving part.
- **Chunking:** semantic chunking (split on headings, sentences) over fixed-size. Edtech content has natural structure.
- **Retrieval:** hybrid (BM25 + vector) for short queries, vector-only for paragraph-length queries.
- **Reranker:** Cohere Rerank or a cross-encoder model. Doubles quality for ~$1/1k queries. Worth it.
- **Generation:** Claude with retrieved chunks in context, instructed to cite source IDs.

### The failure mode you mention unprompted

"Lost in the middle" — models attend less to content in the middle of long contexts. Mitigation: rerank to keep top 3-5 chunks, put the most relevant one at the top.

---

## 6. Tool use / function calling — the protocol-level answer

If they go deep:

- **Anthropic's tool_use** sends `{type: "tool_use", id, name, input}` blocks; you send back `{type: "tool_result", tool_use_id, content}`. Multi-tool calls in a single turn are supported via parallel tool blocks.
- **OpenAI's function calling** is similar but with `tool_calls` array on the assistant message and `role: "tool"` on the response.
- **Gemini's function calling** is similar to OpenAI.

You've worked with Anthropic's. Be honest if they ask about OpenAI's — "I've used both, Anthropic's is what I reach for production-side."

### The gotchas you mention

- Tools with overlapping descriptions degrade selection — write tool descriptions adversarially, emphasizing what makes each *unique*.
- Long tool outputs eat context fast. For tools that return logs or query results, summarize before returning.
- Sequential vs. parallel tool calls — let the model parallelize when tools are independent.

---

## 7. Evals — the question they'll respect you for asking

If they don't bring up evals, *you* bring them up.

> "How are you evaluating grading quality today? Is there a held-out set with human gold labels?"

This signals senior. Most early-stage AI products skip evals until they get burned. Show that you know to build them from day one.

### What an eval suite looks like

- **Golden set:** 50-200 hand-graded answers across difficulty and topic.
- **Metrics:** agreement rate with human (exact + within-1-band), bias delta across student demographics, calibration (does confidence 0.8 actually mean 80% correct?).
- **Regression suite:** runs on every prompt change in CI. Block deploy if metrics drop.
- **Production sampling:** 0.5-1% of live grades go to human review. Drift detection.

If they're not doing this yet, you can offer to set it up in your first 30 days. That's a concrete first win.

---

## 8. Multi-agent orchestration — what you mean by it

The JD mentions "decompose features, dispatch to agents, review rigorously." If they ask what your version of this looks like:

### Your current setup (be specific)

- **Planner agent:** reads the spec, decomposes into atomic tasks, writes a plan.md.
- **Executor agents:** one per task, sandboxed in a worktree, run with Claude Code.
- **Reviewer agent or human:** reviews the diff against the plan and the original spec.
- **Coordinator (you):** approve the plan before execution, review the diffs before merge.

The non-negotiable is the human gate at plan-approval and diff-merge. Agents do the typing; you do the judgment.

### Tradeoffs you've made

- Worktree isolation costs disk and setup time, but it's the only way to parallelize without conflicts.
- Smaller, more atomic tasks beat fewer big tasks. Agents drift on long tasks.
- Reviewing 5 small diffs takes less time than debugging one big drift.

---

## 9. Model selection — when do you reach for what

Be ready to defend a stance.

| Use case | Model | Why |
|----------|-------|-----|
| Cheap routine grading | Claude Haiku 4.5 | Fast, cheap, good enough for short-answer with a rubric |
| Ambiguous grading, escalation | Claude Sonnet 4.6 | Strong reasoning, calibrated confidence |
| Complex reasoning, hard cases | Claude Opus 4.7 | Use sparingly, expensive |
| Embeddings | OpenAI text-embedding-3-small or Voyage | Cheap and good |
| Reranking | Cohere Rerank or local cross-encoder | High ROI on retrieval quality |
| Speech (if they expand to oral exams) | Whisper or Deepgram | Whisper for offline, Deepgram for streaming |

If they ask "why Anthropic over OpenAI?" — your honest answer: stronger structured outputs, better tool-use ergonomics, longer context with less degradation, prompt caching is mature. Not a religion, just current preference.

---

## 10. Live coding / pair prompt — what to expect

If they pair with you, the most likely prompts are:

1. **"Build a tool that takes a question and a student answer and returns a grade."** — start with the schema, not the code. Sketch the prompt, the structured output, the validation, the test. Talk through tradeoffs as you type.
2. **"Add a feature to an existing Next.js + Supabase repo."** — straightforward fullstack, but they're watching how you read unfamiliar code. Start by reading the schema, then the routes, then the components.
3. **"Debug this prompt — it's returning bad outputs."** — look for: missing schema, ambiguous instructions, contradictory examples, no refusal path.

**Think aloud constantly.** Pair coding is judged on reasoning, not speed.

### The things you should never say in a pair

- "I'd just use ChatGPT for this." (Even if true. Demonstrates the work.)
- "I don't really know X." Replace with "I haven't used X in production but here's what I'd do based on Y."
- Silence longer than 30 seconds. Narrate.

---

## 11. Common gotcha questions and answers

### "Are LLMs ready to grade student work?"

> Depends on the task. Multiple choice and short factual answers, yes. Long-form essays graded against multi-dimensional rubrics, with bias audits and human spot-checks, also yes. As the sole grader of high-stakes summative exams without human oversight, no — and I'd push back on any product roadmap that proposed that.

### "How do you handle hallucinations?"

> Three layers. Structured outputs with validation reject malformed answers. Confidence thresholds escalate uncertain cases. Eval suites catch regressions before production. The fourth layer is product design — show students the model's reasoning so they can flag bad grades, treat the grade as a draft until reviewed.

### "What's your take on fine-tuning vs prompting?"

> Prompt first, fine-tune when prompting plateaus or cost gets out of hand. Fine-tuning is right when you have 1000+ labeled examples and a stable task. For grading, the labels come from running Sonnet/Opus and then distilling to Haiku — that's where I'd start.

### "Have you used LangChain / LangGraph / CrewAI?"

Honest version: "I've stayed close to the SDK. The frameworks are useful for prototyping but I've found them harder to debug in production. For my current agent work, I orchestrate with plain Python and Pydantic — explicit beats clever when the agent is touching real systems." (Don't bash them. Just have a reasoned preference.)

### "Where do you see this going in 6-12 months?"

> Small models running locally for routine grading (cost falls to near-zero), better calibrated confidence so escalation is automatic, multimodal grading on handwritten work which matters a lot for WAEC, and longer-horizon agents that can plan a student's whole revision schedule rather than just grade one answer.

---

## 12. Pre-call drill (do this once)

- [ ] Sketch your sysadmin agent's tool list and graph on paper. Time yourself: under 5 minutes.
- [ ] Practice the AI grading system design out loud. Time yourself: 10 minutes end-to-end.
- [ ] Practice the cost math: $0.0006 per grade × students × frequency. Get the unit cost from memory.
- [ ] Pick one *honest weakness* in your AI experience to mention if asked. Pair it with what you'd do about it. (Example: "I haven't shipped RAG to production, only prototyped it. If GLearn needs it, I'd start with pgvector + hybrid retrieval and lean on the team's experience.")
- [ ] Read [story-bank.md](story-bank.md) [AI Agents for Infrastructure Ops] section. Make sure you can tell that story in 90 seconds.

---

## 13. What to ask them on the AI side

Slot these into the questions list in the main prep doc:

1. "What's your current AI stack — model providers, orchestration framework, eval setup?"
2. "How do you measure grading quality today? Is there a held-out set with human labels?"
3. "What's the bottleneck right now — model quality, cost, latency, eval coverage, or something else?"
4. "How do you split work between AI features and core platform work? Same engineers, separate teams, or rotation?"
5. "What's your stance on fine-tuning vs prompting for your stack?"

Asking these signals you've operated at this level. They'll move the conversation from "do you know AI" to "are you the right senior to drive AI here."

---

## Notes scratchpad

- Their actual model provider:
- Their eval setup:
- Their cost concerns:
- Things they got wrong that you can fix:
- Things they got right that you can build on:
