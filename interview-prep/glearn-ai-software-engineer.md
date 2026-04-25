# Interview Prep — GLearn, AI Software Engineer

**Source report:** [003-glearn-2026-04-16.md](../reports/003-glearn-2026-04-16.md)
**AI deep-dive companion:** [glearn-ai-deep-dive.md](glearn-ai-deep-dive.md)
**Application date:** 2026-04-16
**Score:** 4.6/5 (cleanest fit of the 2026-04-16 batch)
**Posture:** Excited but probing. Real company signals + early-stage signals. Verify before committing.

---

## 1. 60-second context refresh

- Ghana/SF edtech, WAEC prep, AI grading + adaptive learning.
- Stack: Next.js + TypeScript + Tailwind + Supabase.
- The role is full-stack with an AI-agent-orchestration core. They want someone who already dispatches work to Claude Code / Cursor agents and reviews diffs rigorously.
- "Core Team, San Francisco & Accra". Likely founder-led, pre-launch, hiring across eng/product/marketing.
- You partner with the founder. Senior-shaped responsibilities even if not titled Senior.

---

## 2. The "tell me about yourself" — GLearn version (90 seconds)

> I'm a senior engineer based in Accra. Computer Engineering at Ashesi, then GTBank where I founded the bank's first DevOps practice — that's the credibility line. The story I'd lead with is MyHealthCop: I was the founding CTO, took it from zero to three apps in production, AWS with GCP for DR, 12-person team. That's the 0-to-1 muscle.
>
> The work I'm most excited about right now is what I do in my own time: I've been building specialized AI agents that run against live production Linux — Claude tool-use, structured outputs, HITL approval gates. It's not a side project, it's how I work. When I read your JD, "decompose features, dispatch to agents, review rigorously" is the exact sentence I'd use to describe my current workflow.
>
> The Ghanaian education context isn't research for me. I went through it. WAEC, Ashesi, the whole shape of it.

---

## 3. Pre-call checklist (do once before the screen)

- [ ] Re-read the JD verbatim. Re-read this doc. Re-read [003-glearn-2026-04-16.md](../reports/003-glearn-2026-04-16.md) Block F.
- [ ] Pull up GLearn careers page in browser. Have it open during the call.
- [ ] Confirm headset + lighting. Test loom-style screen share if they want a code walk.
- [ ] Have your CV (`output/markdown/003-cv-oswald-gyabaah-glearn-2026-04-16.md`) and the AI Agents repo open in side-by-side tabs.
- [ ] Write three numbers on a sticky note: salary floor ($40K), target ($70K-100K), equity floor (0.5%).
- [ ] Note the time: 9am PST = 5pm Accra. Confirm timezone in advance.

---

## 4. Likely interview format

Three rounds is the standard early-stage shape. Plan for:

1. **Founder screen (30-45 min).** Story, fit, why GLearn, comp range. They'll size you up on ownership and energy. This is the call you're prepping for first.
2. **Technical deep dive (60-90 min).** Either a live system-design discussion (recommend) or a take-home with code review. Likely topics: AI agent orchestration architecture, Next.js + Supabase data modeling for adaptive learning, mobile strategy.
3. **Working session / pair programming (60-120 min).** Build a small feature against their codebase, or pair with the founder on a problem. They want to see you work, not just talk about working.

If they propose only one round before offer, that's a red flag for either rushed hiring or low rigor — push for at least the technical deep dive.

---

## 5. Stories to lead with (from story-bank.md)

| If they ask about... | Lead with | Backup |
|----------------------|-----------|--------|
| AI / agents | [AI Agents for Infrastructure Ops](story-bank.md) | Palsar AI Monitoring SaaS |
| 0-to-1 / founding | MyHealthCop 3 React Apps | Virk Cloud (Vercel-class platform) |
| Fullstack chops | MyHealthCop + GTBank OTP Verification | Digital-Recon dashboard |
| Performance / debugging | MyHealthCop DB Optimization | GTBank uptime work |
| System design at scale | MyHealthCop Background Processing | GTBank K8s 800+ pods |
| Leadership / mentoring | GTBank Junior Engineer Training | MyHealthCop 12-person team |
| Mobile | MyHealthCop Flutter (iOS + Android) | Vistara Flutter admin |

**One story per question.** Don't stack three when one will do. Tight beats long.

---

## 6. Technical depth drills (do these)

### a) AI agent architecture — be specific or be exposed

If they ask "what agents have you built?", do not stay abstract. Be ready to name:

- The agents (QA, code review, sysadmin).
- The runtime (Claude API + tool-use, Python orchestrator).
- The boundaries (HITL approval gate before any write to a production server).
- The graph (which agent calls which, where state is shared).
- The failure modes (rate limits, hallucinated tool args, infinite loops) and how you handle them.

If you can't draw the graph on a whiteboard, you're not ready. Practice once.

### b) Next.js + Supabase for adaptive learning

A likely system-design prompt: "Design the data model for a WAEC adaptive learning feature." Practice this aloud once.

- Entities: student, subject, topic, question, attempt, mastery score per topic.
- Auth: Supabase auth with RLS per student.
- AI grading flow: free-text answer → LLM with rubric → structured output (correctness 0-1, rubric breakdown, feedback) → store + update mastery.
- Spaced repetition: SM-2 or similar; questions surface based on mastery decay.
- Realtime: Supabase channels for live progress on dashboards.

You don't need to be a Supabase expert. You need to show you'd reach for the right primitives (RLS, edge functions, realtime, vector for question similarity if they use it).

### c) Convex vs Supabase honest take

Practice the honest comparison from the report. Don't bash either. They'll respect the nuance.

### d) Cost & latency awareness

Edtech for 5M+ students means LLM cost matters. Be ready with: prompt caching, smaller models for routine grading, batched grading for non-urgent flows, fallback chains. Cost-per-graded-answer is a metric you'd track.

---

## 7. Questions to ask them

Pick 4-5. Don't dump all of them.

**On the product:**
1. The "5M+ students" framing — is that the addressable WAEC market, or current/projected active users? What's the metric you track internally?
2. What does the AI grading loop look like today? Is it shipped, in beta, or still in design?
3. What's the relationship with WAEC the body, or with schools? B2C, B2B2C, or hybrid?

**On the company:**
4. Why are you still on the vercel.app domain? (Phrase it as: "I noticed the careers page is on a preview URL — what's the launch timeline?")
5. SF + Accra split — where does eng leadership sit, and where does product sit?
6. Funding stage and runway?

**On the role:**
7. What does the first 30/60/90 days look like for this hire?
8. How do you measure success for this role at month 6?
9. What's the current eng team shape — total size, who I'd partner with, who reviews my code?

**On comp:**
10. (Save for later in the screen, after fit is established.) "For a remote-from-Ghana role at your stage, what does the package look like — salary, equity, or both?"

**On culture:**
11. Walk me through how a feature gets shipped today — from idea to production.
12. How do you handle disagreements on technical direction between SF and Accra?

---

## 8. Red flags to verify before signing anything

1. **Vercel.app domain.** Acceptable for a 6-month-old startup. Concerning if the company claims to serve real students today.
2. **"5M+ students" claim.** Confirm whether this is TAM or DAU.
3. **Funding.** Pre-seed / seed / Series A? Runway in months. Walk away from "we're bootstrapped and figuring it out" if there's no equity.
4. **Equity.** Get the actual percentage, vesting schedule, strike price, 4-year cliff details. "0.5%" with no specifics means nothing.
5. **Founder profile.** Look up on LinkedIn before the call. Cross-check the SF + Accra story.
6. **Customers / pilots.** Any signed schools? Any paid users? "Coming soon" is fine for pre-launch but should be coming soon, not 18 months away.

---

## 9. Salary anchoring script

When they ask: do not give a number first if you can avoid it.

> "Happy to talk numbers. I'd want to understand the structure first — is this primarily salary, primarily equity, or a real mix? And where is the company on funding?"

If they push:

> "For a remote Accra role with senior scope, my range is $70K-100K USD on the salary side, and I'd flex lower for meaningful early-stage equity — say 1-2%. Walkaway is below $40K with no equity. What's the band on your end?"

Memory says comp flexibility is fine for fully-remote-from-Ghana roles. Don't auto-skip on a low cash number if equity is real.

---

## 10. Day-of opening lines

- Opening 60s: "Thanks for making time. I went through the careers page and the role description — the AI agent orchestration line is what pulled me in. I've been building agents against production servers in my own time and the way you frame the workflow matches mine. Excited to talk about whether the fit is real."
- If silence: ask them to tell you about the company first. Founders love telling the story. Listen for what's missing (revenue, users, customers).
- If they go technical first: lead with AI Agents story, not GTBank. Match their energy.

---

## 11. After the call (within 1 hour)

- [ ] Update [data/applications.md](../data/applications.md): change status from `Evaluated` to `Interview` with date and round number in notes.
- [ ] Append a debrief to this file: who you talked to, what they said about funding/equity/users/timeline, what surprised you, what to verify before round 2.
- [ ] Send thank-you email within 24h. Reference one specific thing from the conversation. Two sentences max.
- [ ] If story-bank.md needs a new story (something you said well that's not yet captured), append it.

---

## 12. Walk-away triggers

Pull the cord if:

- They want a 5+ hour unpaid take-home before the first technical conversation.
- They will not name a salary range.
- They cannot describe what's actually shipped today vs. roadmap.
- The "founder" is more recruiter than builder when you talk technical.
- Equity terms are vague after you ask directly.

---

## Notes scratchpad (fill during/after the call)

- Founder name(s):
- Funding stage:
- Headcount:
- Active users / customers:
- Stack confirmed:
- Comp band stated:
- Equity range stated:
- Vibe (1-5):
- Next steps:
