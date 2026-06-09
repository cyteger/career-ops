# Confirmed Facts for cv_master.md

Source: `cv-research/questions-for-oswald.md`, answered by Oswald on 2026-06-05. Everything here is CONFIRMED real. Honor the corrections. Do not inflate, do not invent. Conservative end where ranges were given.

---

## A. GTBank tenure structure (resolves the "two concurrent Lead roles" red flag)
- ONE continuous GTBank tenure, Apr 2024 to Present, with expanding scope.
- Core Banking Services Lead is a "second hat" held simultaneously with DevOps Engineering Lead. It is a scope expansion, not a second competing job.
- Also bank-wide code-review approver: reviews and approves all code-related changes bank-wide.
- Framing: a single GTBank block with stacked/evolving titles and a clear "expanded scope" signal. Do NOT present two separate "Present" jobs.

## B. Solution-architecture / technical-program responsibility (the "missing TPM role")
- An ADD-ON responsibility, not a separate job title.
- Flow: received application requests, gathered and wrote technical requirements, produced HIGH-LEVEL architecture, recommended design and coding approach. Recommendations were NON-BINDING (devs could choose their own approach).
- Owned UAT: validated delivered work with business users for sign-off.
- ~5 projects before handing over to focus on Finacle. All delivered on time.
- Presented to: developers, business users, group head, occasionally CIO and CSO.
- Honest verbs: "defined requirements", "produced high-level designs", "recommended". NOT "owned"/"enforced" architecture. No formal ADRs or design docs.

## C. DevOps practice founding (standards and adoption)
- Founded DevOps team of 4; personally interviewed all team members.
- Built: DevOps adoption roadmaps (dev + application-support teams), git-driven standards, deployment runbooks, Azure DevOps Server pipeline templates.
- Adopted by 2 teams (application development + application support / operations); ~40 apps and counting.
- Org-wide deployment frequency still constrained by bureaucratic change management (multi-stakeholder sign-off). Platform CAPABILITY: 1 deployment / 5 min, around the clock. Frame as capability, not realized frequency.
- 10 apps migrated to Kubernetes; others not container-ready; migration WIP.

## D. Core banking platform (Finacle)
- Finacle 11, fully containerized on Tanzu Kubernetes Grid (TKG). 800+ pods, 1.5M+ daily transactions.
- EOD batch window ~1 hour; occasionally called in to fix long-running / stuck EOD ops (resource exhaustion, pod scaling and bottlenecks).
- Channels through Finacle: internet banking, mobile app, USSD, ATM, POS.
- Integration layer: internal REST middleware + own gateway + microservices (branches, accounts, transactions, cheques, customers) connecting to Finacle solutions. He maintains these.
- Migration (Basis to Finacle): QA role first (10,000+ test cases, 13 modules, 33 apps), assumed operations later. NOT involved in data-migration mapping or Finacle scripting.
- Cutover marquee: 3,000,000+ accounts migrated; planned 3-hour downtime, completed in 2 hours; no major defects (a few minor slipped); no major data loss.

## E. Payments / rails (MONITORING + integration-maintenance side, NOT posting)
- Bank's rails: GhIPSS, mobile money, card/ATM/POS (Postilion switch), RTGS, ACH, SWIFT, OE PAY, remittances (Remitly, Ria, etc.).
- Oswald's role: monitor and maintain the integration applications so business users can post. First responder when SWIFT or standalone postings fail to reach SWIFT / providers. He does NOT post transactions; business users do.
- Honest verbs: "maintain and monitor integrations with...", "first responder for failed settlement/connectivity". NOT "built payment posting".

## F. DR / resilience
- Application-tier DR for 268 apps to a standby DR data center.
- Oracle DB DR: near-zero RPO via Oracle Data Guard real-time replication, OWNED by the DBA team; Oswald coordinates (not hands-on Oracle RAC/ASM/RMAN).
- DC and DR Kubernetes clusters are independent; only applications are synced via Git (FluxCD); underlying clusters managed by VMware.
- Backups: Velero. Restore-test cadence not established; do NOT claim tested restores.
- DR drill results: RPO = 0; RTO = 22 minutes achieved in live drills, improved from 1 hour on first run (designed target 45 min). No real disaster event yet. State as drills.
- Authored DR policy + runbooks; leads bank-wide failover simulations (600+ staff).
- Parallel Jenkins pipelines with selectable primary/DR targets; Harbor image mirroring.

## G. Operational / platform stack (name these inside existing bullets)
- Secrets: External Secrets Operator backed by HashiCorp Vault.
- TLS/PKI: public CA (Sectigo), annual renewal, manual rotation; certs stored in Vault, loaded dynamically by apps (Elasticsearch, Harbor, etc.); mTLS in-cluster via Istio for mesh + downstream apps.
- Service mesh: Istio, deployed for mTLS only. NO advanced traffic management / canary. Do not claim it.
- Storage: NFS over the network; Oswald manages StorageClasses + PVCs; sysadmin manages underlying NFS.
- Networking/CNI: Antrea / NSX-T on Tanzu; NetworkPolicies for namespace segmentation; WAF exists (network team owns).
- Ingress/LB: ingress controllers with Gateway API HTTPRoute + MetalLB (bare-metal L4).
- AuthN/AuthZ: vSphere (vsphere.local) users with delegated auth for clusters; Keycloak for some apps, Active Directory for others.
- Observability: Prometheus, Grafana, Elastic Stack (Filebeat), Sentry; Gatus for uptime/status (most outages detected within 90 seconds).
- Security scanning: Veracode + Trivy; block all findings above medium severity (~10-15 per app); patch-before-deploy with up to a 2-week deferral window for extensive fixes; all deployments scanned.
- Admission control / policy-as-code: only in personal Virk cluster, NOT at the bank.
- Linux / data-center hardware / ESXi admin: OUT of scope (sysadmin team). He operates the platform layer, not the hardware. Keep "operates on-prem Tier III DC" but do NOT claim hardware/ESXi admin.
- Languages: Python + Bash. Go NOT confirmed in production; do not list Go.

## H. Compliance / regulatory
- PCI-DSS scope + audits; ISO 27001; internal + external audits.
- Controls that helped pass audits: credential segregation, incident runbooks, change management, code review/approval process.
- BoG requirements: data residency in-country; primary DC on bank premises; DR site >= 250 km away; regulator-set RTO/RPO (compliance is the mandate).
- Ghana Card verification service = KYC.
- HSM / key ceremony: not indicated; do not claim.

## I. Incidents / reliability numbers
- Detection: most outages within 90 seconds (Gatus).
- Resolution: minutes typically; hours sometimes; occasionally days for escalations.
- Monthly incidents: 0-2.
- Formal SLA/SLO: none. Do NOT invent an SLA. Can cite measured 99.97% uptime but not as an SLA target.
- On-call paging stats: none provided.

## J. Cost
- No measured cost reduction. DROP "cost optimization" as an outcome. Reframe to the activity (multi-cloud provisioning, access control) without implying savings.

## K. Leadership / people
- 13 engineers report to Oswald in total across MyHealthCop + GTBank.
- Personally interviewed all his team members.
- Mentored juniors from general DevOps into core banking service management roles.

## L. MyHealthCop (Founding CTO, Jan 2021 to Mar 2024)
- ~1,000 users + 40+ health professionals when he left (had just gone live, beginning to scale).
- Uptime excellent; no downtime under his watch; fully on AWS.
- DECISION: "1M+ daily background jobs" is NOT realized production volume at ~1,000 users. Reframe to architecture/capacity: describe the SQS/SNS design + multi-provider failover as built-for-scale. Do NOT state a realized daily-jobs number.
- Real scope: 3 apps (patient Flutter, professional Flutter, React admin), AWS EKS/ECS/Lambda, SQS/SNS multi-provider failover, Redis + PostgreSQL latency work, GitHub Actions + Terraform CI/CD, GCP DR mirror.
- 12-person cross-functional team.

## M. Projects (live status, honesty)
- Lodestar (lodestar.cv): FLAGSHIP, LIVE. Feature prominently. What it is: lets users build and manage resumes with integrated LLM review, reframing, and a JD-tailoring feature that tailors a resume to a job description; JDs pulled dynamically from a URL, uploaded files, or raw text paste; portfolio-site and further features planned. Stack: Next.js, Convex. (Located at /Users/oswald.gyabaah/projects/kirates/folio.)
- Vistara: LIVE, complete, just launched to users. Property tenant-assessment platform (renters evaluate housing conditions before signing leases): landing + tenant web app + admin dashboard + Flutter field app. Stack: Next.js, React, TypeScript, Flutter, Codemagic. Treat as live, not WIP.
- Digital-Recon: WIP (building), not live. Strong origin story: built in response to real GTBank reconciliation pain (transactions stuck in ledgers, debits without matching credits and vice versa, failed transfers not auto-reversed needing manual intervention); intended to evolve into a "sidekick" handling what the core banking system does not. Frame as "building", label WIP.
- Virk Cloud: WIP (building), not live. Frame as "building", label WIP. (Lower priority for product-role subsets.)
- Master CV keeps all (it is a superset) but never implies live traffic for the WIP ones (Digital-Recon, Virk). Lead project subsets with Lodestar, then Vistara / Digital-Recon by relevance.

## N. Other experience / timeline
- bandana.com: freelance DevOps Engineer, Oct 2025 to Jan 2026, US timezone (UTC-4/-5). International remote experience. Scope detail pending; keep generic ("freelance DevOps engineering for a US-based team") until confirmed.
- National service + freelance projects: ~May 2020 to Jan 2021 (fills the post-graduation gap).
- Ashesi University, BSc Computer Engineering, 2016-2020 (unchanged).

## O. Certifications
- HOLD (keep as listed, self-study): AI Engineering Specialization (ByteByteAI), Oracle Certified DevOps Professional, Oracle Certified Architect Associate, Oracle Certified Foundations Associate, AWS Certified Cloud Practitioner, Django Web Framework (Coursera). Oracle certs are standalone self-study; do NOT rename to OCI/Tanzu/Finacle.
- IN PROGRESS: CKA, CKS, AWS Solutions Architect Associate (SAA), AWS Solutions Architect Professional (SAP), Google Cybersecurity (Coursera). Previously studied GCP Professional Cloud Architect (did not sit exam).
- DROP TOGAF entirely (not pursuing).

## P. Community / writing
- Owner of "risingEngineers" Substack; publishes engineering articles.
- MC / Moderator at a 2025 Microsoft event (exact event name pending; keep generic, e.g. "MC / moderator, Microsoft community event, 2025", until confirmed).

## Q. Positioning / title
- Titles Oswald would accept: DevOps Engineer, Solutions Architect.
- DECISION: default master title is "DevOps/Platform Engineer | Solutions Architect" (swappable per application). Supports both accepted titles, with platform/SRE and full-stack as secondary.
- No timezone line on the CV (he declined). bandana.com US-timezone work demonstrates remote overlap implicitly.
- No EA-pivot framing language; position on direct experience. TOGAF dropped.

---

## Anti-inflation checklist (the pressure-test MUST enforce)
1. MyHealthCop daily-jobs number reframed to architecture/capacity, no realized number (not 1M at ~1k users).
2. Payments = monitoring/maintenance, not posting.
3. Oracle DB = DBA-owned; he coordinates.
4. Istio = mTLS / install only.
5. Policy-as-code / admission control = Virk only, not the bank.
6. No hardware/ESXi/bare-metal admin claims (operates platform, not hardware).
7. No SLA/SLO claim (none formal); no cost-savings claim (none measured).
8. DR RTO = 22 min achieved in DRILLS (no real disaster); RPO 0; designed 45 min.
9. WIP projects (Digital-Recon, Virk) not described as live; Lodestar and Vistara are live.
10. Architecture work = "recommended / non-binding", no ADRs. Not "owned/enforced".
11. Go not listed (unconfirmed).
12. TOGAF dropped.
