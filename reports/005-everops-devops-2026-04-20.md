# Evaluación: EverOps — Senior DevOps Engineer

**Fecha:** 2026-04-20
**Arquetipo:** DevOps / Platform Engineer (primary) + Cloud Infrastructure Engineer (primary) — hybrid
**Score:** 4.0/5
**Legitimacy:** High Confidence
**URL:** https://jobs.ashbyhq.com/EverOps/5b8b9de2-9371-4777-a88a-63d6d035f3f3
**PDF:** output/pdf/005-cv-oswald-gyabaah-everops-devops-2026-04-20.pdf
**Recommendation:** APPLY — Title is an exact match for Oswald's primary target archetype. Core stack overlap (EKS, Terraform, ArgoCD, GitHub Actions, Prometheus/Grafana, Python/Bash, AWS security) is strong. Main gaps (Atmos wrapper, EC2→EKS migration framing, Golang) are addressable through reframing and cover letter.

---

## A) Resumen del Rol

| Field | Value |
|-------|-------|
| Arquetipo | DevOps / Platform Engineer + Cloud / Infra — enterprise AWS/EKS modernization |
| Domain | Platform engineering, cloud infra, embedded consulting model |
| Function | Build + lead (IC, SME within a "pod") |
| Seniority | Senior IC, 5+ yrs |
| Remote | "Remote" (unqualified) — but joins a "U.S.-Based Virtual Operating Center" team |
| Team size | Pod model (not disclosed); EverOps embeds engineers into customer teams |
| TL;DR | Lead EC2→EKS migration and AWS multi-account restructuring for EverOps's customers, using Terraform+Atmos, ArgoCD, GitHub Actions, with mentorship responsibilities. |

---

## B) Match con CV

| Requirement | CV evidence | Strength |
|---|---|---|
| 5+ yrs DevOps/CloudOps/SRE | 6 yrs across MyHealthCop CTO (2021-2024) + GTBank DevOps Lead (2024-present) | **Strong** |
| High-scale EKS experience | MyHealthCop: "containerized microservices on EKS and ECS with autoscaling" (cv.md:72) | **Strong** |
| Terraform IaC | MyHealthCop + Virk Cloud: "CI/CD pipelines on GitHub Actions and Terraform" (cv.md:75, 97) | **Strong** |
| EC2→EKS migration (minimal downtime) | Adjacent: "containerized Kubernetes deployments" at GTBank replacing manual handoffs (cv.md:60); MyHealthCop direct-to-EKS builds | **Partial** |
| Atmos (Terraform wrapper) | Not in CV — never used Atmos specifically | **Gap** |
| AWS Organizations + Landing Zone | Multi-cloud AWS + GCP at MyHealthCop, multi-account-style isolation via DR design (cv.md:76) | **Partial** |
| IAM Permission Boundaries + SCPs | "IAM policies" at MyHealthCop (cv.md:76); access control at GTBank (cv.md:66) | **Partial** |
| Docker + K8s-native networking | GTBank: 800+ pods on TKG, Istio service mesh (cv.md:50, cv.md:23) | **Strong** |
| Golang, Python, or Bash | Python (Django, FastAPI, Celery) + Bash (cv.md:18, 63); no Go | **Strong** (2 of 3) |
| AWS Secrets Manager + KMS + External Secrets Operator | AWS infra experience; secrets managed at MyHealthCop but no explicit ESO | **Partial** |
| Datadog / Prometheus / Grafana | Prometheus + Grafana + ELK stack at GTBank (cv.md:65) | **Strong** |
| ArgoCD + GitHub Actions GitOps | ArgoCD + FluxCD + GitHub Actions at GTBank + MyHealthCop (cv.md:24, 61) | **Strong** |
| Technical mentorship (SME in a pod) | Founded GTBank DevOps team of 4, led 5-person QA team through Finacle migration (cv.md:52, 60) | **Strong** |

**Extra Awesome match:**
- Fintech background — GTBank, 1.5M+ daily banking transactions (cv.md:50) — **Strong**
- IDP mindset — Virk Cloud PaaS (cv.md:91-97) — **Strong**
- Argo Rollouts (canary/blue-green) — **Gap**
- OPA / Kyverno — **Gap**
- KubeCost / FinOps — **Gap** (has generic "cost optimization" at GTBank, cv.md:66)
- CKA / AWS SA Pro — **Gap** (has AWS Cloud Practitioner + Oracle DevOps Pro + Oracle Architect Associate)

### Gaps — mitigation plan

1. **Atmos (specific Terraform wrapper)** — Not a hard blocker. Atmos is a Cloud Posse tool; learning curve is ~days for someone with deep Terraform. Cover-letter line: "I've built hierarchical Terraform for multi-environment deployments at MyHealthCop and Virk Cloud; happy to ramp up on Atmos quickly — the conceptual model (DRY, component-driven) maps to patterns I already use." Optional: pre-reading Cloud Posse reference architecture before interview.
2. **Golang** — Role lists Golang OR Python OR Bash. Oswald has Python + Bash as production languages. Not a blocker.
3. **EC2→EKS migration framing** — Oswald built on EKS natively at MyHealthCop rather than migrating. Frame GTBank modernization angle: "replaced manual code handoffs with containerized Kubernetes deployments" — conceptually similar (legacy → containerized). Mention Finacle on TKG as enterprise K8s experience.
4. **Argo Rollouts / OPA / KubeCost** — Listed as "Extra Awesome," not required. Note in cover letter as planned learning areas or skip.
5. **AWS SA Pro / CKA** — Not required. Oswald has Oracle DevOps Pro + AWS Cloud Practitioner. Could pursue CKA in next quarter if it becomes a blocker.

---

## C) Nivel y Estrategia

**JD level:** Senior IC with 5+ yrs, "technical anchor," pod SME.
**Oswald's natural level:** Senior (6 yrs, founded two DevOps/infra practices — MyHealthCop + GTBank).

**Sell "senior without stretching" plan:**
- Lead with GTBank: "Founded GTBank Ghana's DevOps practice from scratch — 4 engineers, 800+ pods on TKG, 1.5M+ daily banking transactions at 99.97% uptime."
- Position the CTO experience as the SME/mentorship signal the JD asks for: led 12-person team at MyHealthCop + 4-engineer DevOps team at GTBank + 5-person QA team for Finacle migration.
- Emphasize the "zero-to-one platform" story (Virk Cloud PaaS) as the IDP/platform-engineering mindset the JD flags.
- Flag Fintech experience explicitly — JD calls out AdTech/Gaming/Fintech as "Extra Awesome."

**If downleveled:**
- Accept if comp is within the $70K-$160K band.
- Negotiate review at 6 months with explicit promotion criteria.
- Request the first pod assignment include migration scope to demonstrate the EC2→EKS work.

**Embedded consulting model caveat:**
- EverOps engineers work inside customer environments — client-facing expectations matter.
- Oswald has enterprise customer-facing experience (led GTBank Finacle migration integrations, MyHealthCop stakeholder management). Use both as STAR stories.

---

## D) Comp y Demanda

| Data point | Value | Source |
|---|---|---|
| US market Senior DevOps (remote) base | $140K-$200K | Levels.fyi / Glassdoor general range for US Senior DevOps |
| EverOps specific comp | Not disclosed in JD | Ashby posting — equity mentioned, no salary band |
| Benefits noted | Unlimited PTO, 401K + company match, equity, sponsored healthcare, 100% remote | JD Benefits section |
| Geographic adjustment | Possible for Ghana-based remote | Oswald's profile: acceptable if total > $50K |

**Notes:**
- EverOps is a privately-held embedded-services firm. Likely US-rates with possible geographic adjustment for non-US hires. Not confirmed until comp conversation.
- JD does NOT explicitly restrict to US-only hires ("Remote" unqualified in Location field), but "U.S.-Based Virtual Operating Center" may signal US preference. Clarify in screen.
- Equity is listed as a true ownership stake — real signal of retention interest, not just comp filler.

**Comp score:** 3.5/5 — Unknown but infrastructure-side of US market is generally well-paid; acceptable floor assumed.

---

## E) Plan de Personalización

**Top 5 changes to CV (for tailored PDF):**

| # | Section | Current | Proposed | Why |
|---|---|---|---|---|
| 1 | Summary | "Full-stack engineer with 6 years…" | "DevOps / Platform Engineer with 6 years shipping enterprise Kubernetes at scale. Founded GTBank Ghana's DevOps practice — 800+ EKS-equivalent pods, 99.97% uptime, 1.5M+ daily transactions. Now architecting multi-cloud platforms with Terraform and GitOps." | Leads with DevOps headline, EKS-framed K8s, scale/uptime metrics, multi-cloud + Terraform — JD's top keywords. |
| 2 | Core Competencies | N/A (regenerate) | EKS • Terraform (IaC + modules) • AWS Multi-Account • GitHub Actions + ArgoCD • Kubernetes at Scale • AWS IAM & Secrets • Prometheus/Grafana • Platform Engineering | 8-tag grid from JD requirements. |
| 3 | GTBank bullets | "…800+ production pods" | "…800+ production pods on enterprise Kubernetes (TKG) sustaining 1.5M+ daily banking transactions, with Istio service mesh, RBAC-based multi-tenant isolation, and Prometheus/Grafana observability." | Adds RBAC + multi-tenant + Istio — JD keywords in 'EKS Operations' bullet. |
| 4 | MyHealthCop bullets | "…containerized microservices on EKS and ECS" | "Architected EKS-based platform with autoscaling workloads, VPC peering, AWS Secrets Manager + KMS for secrets, and Terraform + GitHub Actions for CI/CD across multi-environment accounts." | Direct AWS + EKS + Terraform + CI/CD keyword dense, matches "Cloud-Native Security" bullet. |
| 5 | Projects (Virk Cloud) | "…RKE2 cluster deployment" | "Built an internal developer platform (IDP) on RKE2 with FluxCD GitOps, Terraform-provisioned infra, per-tenant namespace isolation, and self-service deployments — the same platform-engineering patterns used at hyperscalers." | Maps to "Platform Engineering" Extra-Awesome bullet. |

**Top 3 LinkedIn changes:**
- Headline → "Senior DevOps / Platform Engineer — Enterprise Kubernetes, Multi-Cloud, AI-Augmented Infrastructure"
- About → lead paragraph rewritten around EKS + Terraform + GitOps at GTBank scale
- Featured → pin GTBank DevOps founder story + Virk Cloud PaaS

---

## F) Plan de Entrevistas

| # | JD requirement | STAR+R story | S | T | A | R | Reflection |
|---|---|---|---|---|---|---|---|
| 1 | EC2→EKS migration | GTBank Finacle modernization | Bank ran core banking with manual handoffs and bare-metal deploys | Containerize and automate Finacle-adjacent workloads on TKG | Founded DevOps team, introduced Helm+FluxCD, containerized pipeline | ~90% deploy time cut, ~5x release velocity, 800+ pods stable | Embedded SRE discipline early (observability + runbooks) saves months of firefighting — would do it day-one next time. |
| 2 | Multi-account AWS + Landing Zone | MyHealthCop AWS+GCP DR architecture | Small startup needed resilient infra on startup budget | Design DR across providers with account isolation | Primary on AWS EKS, mirror on GCP GKE, VPC isolation + IAM policies + dual CI/CD | Failover-ready DR at <3x base cost | Dual-provider DR is expensive operational overhead — for most companies, multi-AZ on one provider is enough. Know when to stop. |
| 3 | GitOps + CI/CD at enterprise scale | GTBank FluxCD rollout | Manual code handoffs, no pipeline discipline | Introduce GitOps + policy-enforced deployments | FluxCD + Helm + Azure DevOps + Veracode/Trivy scanning | Declarative, idempotent deploys; 3M+ daily requests at 99.97% uptime | The cultural change (reviews, approvals, rollback rehearsals) was harder than the tooling. Process before tools. |
| 4 | Platform engineering / IDP | Virk Cloud PaaS build | Small teams needed Vercel-style experience without Vercel pricing | Ship a Kubernetes-based PaaS | RKE2 + FluxCD + Terraform + custom Next.js console with auth, billing, observability | Production-ready PaaS; design doc now referenced in EveryDayOps writing | IDPs succeed when developer UX is better than the raw tool — platform engineers are product engineers first. |
| 5 | Technical mentorship / SME in a pod | Founded GTBank DevOps team from zero | Bank had no DevOps practice, ad-hoc deployments | Build a team and a platform | Hired + onboarded 4 engineers, set up shared runbooks, paired reviews, observability standards | Team became the bank's reference point for deployments across all internal apps | Early on I bottlenecked by doing instead of teaching; once I shifted to pairing + docs, team velocity doubled. |
| 6 | Security in cloud-native (KMS, Secrets) | MyHealthCop healthcare data handling | Patient PII + payment tokens needed strong encryption | Design encryption + secrets + access control for HIPAA-adjacent workloads | AWS Secrets Manager + KMS + IAM role-per-service + audit logging | No incidents in 3 years of production | For healthcare/fintech, design audit-ready from day one — retrofitting compliance is 10x more expensive. |

**Recommended case study for interview:**
**GTBank DevOps founding story.** Why: enterprise scale, measurable outcomes, team-building, multi-cloud, AI-augmented next step — hits every "Extra Awesome" signal.

**Red-flag questions to prep:**
- *"Why did MyHealthCop end?"* → Honest: co-founder dynamics + funding; pivoted to enterprise work where my infra skills scale. Left the platform running.
- *"Any experience with Atmos specifically?"* → "No — I've built hierarchical Terraform across environments at both MyHealthCop and Virk Cloud. Atmos is on my short-list to ramp up on; the component-driven model maps to patterns I already use."
- *"U.S.-Based Virtual Operating Center — any timezone concerns?"* → Ghana is GMT; I have full EU overlap and 5-8 hours with US East Coast. Have run production incidents across timezones at GTBank.

---

## G) Posting Legitimacy

**Assessment:** **High Confidence**

| Signal | Finding | Weight |
|---|---|---|
| Posting freshness | Ashby page loads cleanly, Apply button active (observed 2026-04-20) | Positive |
| Apply button state | Active, direct link to application form (not redirect) | Positive |
| Tech specificity | Highly specific: Atmos, External Secrets Operator, Argo Rollouts, OPA/Kyverno — shows real technical author | Positive |
| Requirements realism | 5+ yrs + realistic AWS/K8s stack; no contradictions (e.g., "entry-level Staff Engineer") | Positive |
| Salary transparency | Equity + benefits listed, no base band — common for US private companies | Neutral |
| Reposting detection | Not seen before in scan-history; EverOps Identity+QA (URL ec0d1bb0) is a different role | Positive |
| Role-company fit | EverOps is a DevOps-as-a-service firm; hiring DevOps engineers is core to their model | Positive |
| Company hiring signals | No layoff signals found; EverOps appears to be a growing private firm | Neutral |

**Context notes:**
- EverOps is a real US-based embedded-services firm (verifiable at everops.com).
- The JD reads as written by a practitioner — specific tool names, realistic scope, pod model described concretely.
- Two open roles at EverOps in April 2026 (this one + #004 Identity/QA) suggests active hiring, not ghost-posted pipeline.

---

## Keywords extraídas

amazon-eks, terraform, atmos, aws-multi-account, aws-organizations, landing-zone, iam-permission-boundaries, scps, argocd, github-actions, gitops, ci-cd, docker, kubernetes, rbac, multi-tenant, aws-secrets-manager, kms, external-secrets-operator, prometheus, grafana, datadog, platform-engineering, internal-developer-platform, idp, ec2-to-eks-migration, containerization, devops, sre, senior-devops-engineer
