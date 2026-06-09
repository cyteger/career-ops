# Master CV Framing Brief — Oswald Gyabaah

Style contract for every rewrite: plain, direct, human. No em dashes. No marketing-speak. No buzzword soup. Every number auditable, every claim survivable in a reference check. When he only remembers a range, use the conservative end.

This is a MASTER CV — a superset library that is never submitted as-is. Build it so titles, summary lines, experience order, skills, and projects are clean **swap fields** he subsets per application.

---

## 1. Title strategy

Retire "Full-Stack Software and Infrastructure Engineer" as the default. It tries to be everything and lands as nothing at his seniority.

**Master default (neutral anchor):** `Senior Platform & Infrastructure Engineer`
(alternate acceptable anchor: `Platform Engineer & Solutions Architect`)

**Render a target-specific title per application:**
- Platform / SRE / DevOps: `Senior Platform / DevOps Engineer`
- Solutions Architect: `Solutions Architect (Platform & Cloud)` or `Infrastructure / Solutions Architect`
- Full-stack / product: `Full-Stack Engineer (React / Next.js / Python)`
- Leadership: `Engineering Lead / Founding CTO`

The exact title he most wants to be called for should come straight from the target posting. Treat the title as data, not a fixed string.

---

## 2. Summary rewrite guidance

Cut every adjective that cannot be measured. Drop "at scale," "production systems at scale," and loose "end to end." Lead with the unfakeable proof, not a generic discipline label.

Target shape (three sentences, fact-first):
1. What he is + the rarest credential: owns the Finacle core banking deployment behind 1.5M+ daily transactions at GTBank Ghana, including its 268-application disaster recovery at a 45-minute RTO.
2. Founded the bank's DevOps practice from scratch.
3. Earlier, founding CTO of MyHealthCop, building mobile, web, and backend end to end.

Each rendered subset reorders these: platform subset leads with the infra proof; architect subset leads with the TPM/architecture role + DR + integrations; product subset leads with the CTO/full-stack range.

Caution: do not lead the master summary with "solutions architect" until the TPM/architecture role is on the CV to back it. Right now the claim floats without a titled architecture entry. Once the TPM role is added, the architect framing is earned.

---

## 3. Section order

For a senior candidate, Experience is the proof and must come first. Recommended order for the master and every render:

`Summary → Experience → Selected Projects → Skills → Certifications → Education`

- Move Experience above Skills. A wall of ~90 tools before the GTBank work signals junior "I know many things."
- Demote the entry-level certs (AWS Cloud Practitioner, Oracle Foundations) below the strong experience; they currently over-weight.
- Keep the full skills superset in the master file. Every submitted subset trims to ~12–15 tools matched to the target stack. Add a dedicated "Core Banking & Payments" skills line (Finacle, EOD/BOD batch, Oracle Data Guard, GhIPSS, mobile money, ISO 8583/20022, SWIFT, RTGS/ACH, HSM, ESB/API gateway) that banking/fintech subsets turn on and remote-infra subsets turn off — list only what he confirms.

---

## 4. Breadth vs sharpness strategy

The master stays broad and complete; sharpness comes from subsetting, not from cutting the library.

- **Give the CV a spine.** One organizing throughline turns five parallel threads into a progression: build systems, operate them at scale, then lead the teams and architecture around them. The undocumented TPM/architecture role is the connective tissue that makes the arc legible — add it as its own dated entry between CTO and DevOps Lead.
- **Resolve the two GTBank Lead roles structurally.** If it was a promotion, nest both titles under one GTBank header with a progression line (DevOps Lead 2024–2025 → Core Banking Services Lead 2025–present). If he holds both, add one explicit line: "expanded scope to core banking platform ownership in May 2025 while retaining DevOps leadership." Eliminate the two side-by-side "Present" end-dates.
- **Rank projects by traction, demote the rest.** Master keeps all five. Each project needs one outcome/traction line answering "is anyone using this?" Lead infra/product renders with at most the two most relevant that have proof (Vistara TestFlight, Virk Cloud live infra, Digital-Recon for fintech). Drop erifoundry and zero-traction projects from infra/architect subsets — they are filler there.
- **Order experience by relevance when subsetting.** Build the master so these are clean cuts, not rewrites.
- **Keep the AI/agents thread as a growth signal, not implied production experience.** Make the side-project time commitment honest so founder-stacking does not read as inflation.

---

## 5. Buzzword and red-flag fix list (all lenses)

1. **"at scale" / "production systems at scale" / loose "end to end"** — delete or replace with the specific system and number.
2. **"Architected integrations between Finacle and third-party systems including transaction portals and internal tools"** — the single weakest, least verifiable line. Replace with named rails (GhIPSS, MoMo) and named middleware (ESB/API gateway) plus a count and the volume they carry, or cut.
3. **"Introduced a unified observability stack... reducing mean time to resolution"** — replace the vague clause with the actual MTTR delta.
4. **"access control and cost optimization"** — quantify the cost work (percentage, consolidation count, tool like Kubecost) or cut. Currently the softest filler on the CV.
5. **"Near-zero RPO"** — name the mechanism (Oracle Data Guard) or soften. Asserting it with no mechanism invites an immediate banking-interview probe.
6. **Round-number cluster (90% twice, 95%, 99.97%, 5x)** — convert to auditable before/after or cite the measurement source. Fix the duplicate 90% (deploy time and latency) so it does not look like a reused template figure.
7. **99.97% uptime** — frame against an SLA/SLO with a measurement window and tool, not as a bare metric.
8. **Istio Service Mesh** — substantiate with concrete mesh work (mTLS, traffic policy, telemetry) or move it out of the headline skills line. As written it reads as keyword-stuffing next to genuinely deep work.
9. **FluxCD GitOps with no secrets story** — name the secrets strategy (Sealed Secrets / External Secrets / Vault). Its absence makes a strong claim look incomplete.
10. **Bare-metal / Tier III / VMware in the skills line only** — back it with an experience bullet (vSphere/ESXi work, DR-site hardware) or it reads as an unsupported keyword.
11. **AI agents framed as pure R&D** — tie to real usage in GTBank ops if true, or keep explicitly as a growth/learning signal so it does not read as resume-driven development.
12. **Summary "solutions architect" with no titled architecture role** — back it by surfacing the TPM/architecture role first.
13. **Two concurrent "Present" GTBank roles** — add a progression or scope-expansion marker.
14. **Founder-title stack** — give each project a traction line or accept demotion in subsets.
15. **erifoundry bullets** ("AI-driven research," "cognitive modeling," "human-centered learning systems") — vaguest content in the document. Tighten to something concrete or keep out of infra/architect renders.
16. **"6 years" vs "5+" mismatch** — pick one defensible number, keep it consistent across every subset.
17. **Title mismatch** — "Core Banking Services Lead" (CV) vs "Manager, Finacle Services Team" (memory). Pick one; a recruiter will cross-check LinkedIn.
18. **Unexplained May 2020–Jan 2021 gap** — name it (national service / freelance / early MyHealthCop) to remove the silent question mark.
19. **"AI Engineering Specialization, Mar 2026"** — if not yet earned at render time, mark "expected Mar 2026"; never present a future-dated credential as already held. (Current file dates appear consistent with today, but enforce this rule on every render.)
20. **Oracle certs listed generically** — name the actual track (e.g. "Oracle Cloud Infrastructure 2025 Architect Associate") so three certs from one window do not read as a padded bundle.

> Already fixed: the pasted "Lodestar" onboarding email that earlier analyses flagged at lines 131–136 is gone; the file ends cleanly at line 129. No action.

---

## 6. ATS notes

- Keep the dense tool keywords (good for ATS) but seed the role/outcome phrases filters and recruiters actually search where they are true: `site reliability`, `SLO`, `SLA`, `on-call`, `incident management`, `infrastructure as code`, `high availability`, `platform engineering`, `cloud architecture`, `disaster recovery`, `mentoring / team lead`.
- When CKA and AWS SAA are earned, move them to the top of the cert block for international remote applications — the two credentials most likely to clear automated K8s/AWS keyword filters for his primary archetype.
- Add an "In Progress / Expected" cert subsection to house TOGAF (with a target date) and anything mid-flight, signaling the architect pivot honestly without overclaiming.
- For Ghana banking/fintech applications, lead the cert block with Oracle Architect + any Finacle/banking-infra credentials and the Core Banking & Payments skills line. For international remote platform roles, lead with CKA/AWS SAA/Terraform. Keep TOGAF visible in both.
- For international remote targets, add the one-line remote/timezone signal near the header: "Open to remote. Based in Accra (GMT), strong overlap with EU and US-East." GMT is a genuine selling point against US-Pacific candidates.
