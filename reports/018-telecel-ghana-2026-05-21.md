# Evaluation: Telecel Ghana — IT Infrastructure Architect

**Date:** 2026-05-21
**URL:** https://www.linkedin.com/jobs/view/4415071589/
**Archetype:** Cloud / Infrastructure Architect (Enterprise Architecture)
**Score:** 4.1/5
**Legitimacy:** High Confidence
**PDF:** [output/pdf/018-cv-oswald-gyabaah-telecel-ghana-2026-05-21.pdf](../output/pdf/018-cv-oswald-gyabaah-telecel-ghana-2026-05-21.pdf)

---

## A) Role Summary

| Field | Value |
|-------|-------|
| Archetype | Cloud / Infrastructure Architect — Oswald's primary archetype, elevated to Architect level |
| Domain | Enterprise IT infrastructure at a major telecom — on-prem + cloud, data centers, networks, storage |
| Function | Architect + design + govern (standards, reviews, technical approvals) |
| Seniority | Mid-Senior level |
| Remote | On-site, Accra, Ghana |
| Company | Telecel Ghana — formerly Vodafone Ghana; acquired by Telecel Group (2023, $900M); rebranded 2024 |
| Comp | Not disclosed (standard for Ghana market) |
| TL;DR | A major telecom wants an infrastructure architect to design and govern its on-prem + multi-cloud estate — data centers, networks, virtualization, cloud — as it modernizes post-acquisition. |

---

## B) Match with CV

| JD Requirement | CV Evidence | Verdict |
|----------------|-------------|---------|
| More than 5 years in IT Network/Infrastructure architecture, telecom or comparable enterprise-grade env | 6 years (cv.md:11). GTBank = enterprise-grade ("comparable") — core banking, 800+ pods, 3M+ daily requests | ✅ **Met** (first role in this batch where tenure clears) |
| **Skilled in AWS, GCP, Azure AND OCI — a must** | cv.md:22 (AWS EKS/ECS/Lambda; GCP GKE/Cloud SQL; Azure; OCI) — all four. Three Oracle certs directly back OCI | ✅ **Hero match** (rare 4-for-4) |
| Cloud certification required | AWS Certified Cloud Practitioner + 3 Oracle Cloud certs (DevOps Professional, Architect Associate, Foundations) | ✅ Strong |
| Architecting highly available infra — compute, storage, network, virtualization, security, cloud | cv.md:60 (HA K8s clusters, 99.97% uptime, auto-scaling, self-healing); cv.md:70 (EKS/ECS) | ✅ Strong |
| Infrastructure automation & DevOps (Terraform, Ansible, CI/CD) | cv.md:24 (Terraform, Ansible, GitHub Actions, FluxCD, ArgoCD); cv.md:61 (95% config mgmt automation) | ✅ **Hero match** (core strength) |
| Disaster recovery, backup, high-availability architecture | cv.md:74 (DR strategy — AWS primary mirrored to GCP, dual-environment CI/CD, rapid failover) | ✅ Strong |
| Virtualization (VMware, Hyper-V, KVM) | cv.md:22-23 (VMware, VMware vSphere; Tanzu Kubernetes Grid = VMware TKG); KVM via RKE2/VPS | ✅ Strong (VMware especially); Hyper-V not explicit |
| Data centers | cv.md:22 (on-prem bare metal, Tier III data centers) | ✅ Strong |
| Capacity trends, scaling strategies, performance optimization, lifecycle management | cv.md:60-63 (auto-scaling, observability); cv.md:72 (90% latency reduction) | ✅ Strong |
| Operating systems (Windows Server, Linux) | Linux — extensive (cv.md:104-108, all K8s work). Windows Server not explicit | ✅ Linux strong; Windows gap |
| Identity and access management | cv.md (AWS IAM, OAuth2/Keycloak, OIDC, LDAP, JWT) | ✅ Strong |
| Architecture standards, governance, reviews, technical guidance | Lead + founding CTO roles; cv.md:51 (architected integrations); sets standards for teams | ✅ Good |
| Data & AI Certifications | AI Engineering Specialization (ByteByteAI, Mar 2026) | ✅ Met |
| BSc Computer Science / EE / Telecoms or equivalent | BSc Computer Engineering, Ashesi University (cv.md:124) | ✅ Met (equivalent) |
| Networking (LAN/WAN, SD-WAN, firewalls, load balancers) | Cloud networking yes (VPC, VPC peering, WAF, load balancing); classic enterprise/telecom networking (SD-WAN, physical firewalls) not on CV | ⚠️ Gap (cloud-native networking, not carrier/enterprise networking) |
| Excellent knowledge of telecommunication networks | No telecom experience | ⚠️ Domain gap |
| Cisco Certifications (CCNA / CCNP Enterprise) | None | ❌ Gap |
| Security Certifications (CISSP / CompTIA Security+) | None (has security *exposure* — Veracode, Trivy, KYC, WAF — but not the named certs) | ❌ Gap |
| TOGAF (Enterprise Architecture) | Not held. Note: Oswald plans to self-study TOGAF | ❌ Gap (on his roadmap) |

### Gaps & Mitigation

| Gap | Hard blocker? | Mitigation |
|-----|---------------|-----------|
| Telecom domain / telecom networking | Soft. The JD says "telecom **or comparable enterprise-grade environment**" — banking qualifies. The role is *IT infrastructure* architecture (data centers, cloud, servers), not carrier/radio-network architecture. | Frame GTBank as the comparable enterprise-grade environment: core banking at 1.5M+ daily transactions, 800+ pods, multi-cloud, Tier III data centers. Acknowledge telecom is new but the infrastructure architecture transfers directly. |
| Classic enterprise networking (LAN/WAN, SD-WAN, firewalls, load balancers) | Soft. Real gap vs a pure networking architect, but this is an *infrastructure* architect role spanning compute/storage/cloud/virtualization too. | Lead with cloud networking depth (VPC design, private VPC links to on-prem, WAF, load balancing) and on-prem cluster networking. Be honest that SD-WAN/physical-firewall depth is lighter — frame as a fast-ramp area, not a strength claim. |
| Cisco CCNA/CCNP, CISSP/Security+ certs | Soft-to-moderate. Listed under "Must have", but the section opens with "Professional qualifications... **or equivalent industry experience**." | Don't fake them. Lean on equivalent experience: bank-grade security operations, security scanning in CI (Veracode, Trivy), IAM, KYC. If serious about the role, CCNA is a ~6-8 week study target worth mentioning as in-progress. |
| TOGAF | Soft. Listed under "Must have". | Oswald already intends to self-study TOGAF — mention it as actively in progress. His Oracle Certified Architect Associate is a credible adjacent architecture credential to cite now. |
| Windows Server, Hyper-V | Minor. | Linux depth is extensive; Windows Server is a learnable ops surface, not an architecture blocker. |

**Reading:** This is Oswald's strongest CV match of the recent batch. He clears the tenure bar (6 vs 5+), hits the explicit four-cloud "must" (AWS+GCP+Azure+OCI) with Oracle certs backing OCI, and the IaC/DevOps-automation and DR/HA requirements are his core strengths. The gaps cluster in two honest places: (1) classic telecom/enterprise *networking*, and (2) named certs (Cisco, CISSP, TOGAF). None is a hard blocker — the JD explicitly allows "equivalent industry experience" — but the networking-domain gap is the one a sharp interviewer will probe.

---

## C) Level and Strategy

**JD level:** Mid-Senior, 5+ years, architect-level. Designs and governs, not just builds.
**Oswald's natural level:** Strong fit. He has 6 years, is currently a Lead at a major bank, was a founding CTO, and has done architecture across multi-cloud, on-prem K8s, and DR. "IT Infrastructure Architect" is his primary archetype made explicit — this is not a stretch role, it is a natural next title.

### Sell senior without lying
- This is the role where he should be **confident, not apologetic** — it is squarely his lane. Lead with: founded a bank's DevOps practice, architected HA Kubernetes at 99.97% uptime over 3M+ daily requests, designed multi-cloud DR (AWS mirrored to GCP), and runs core banking infrastructure at 1.5M+ daily transactions.
- The **four-cloud fluency (AWS/GCP/Azure/OCI)** is a genuine differentiator — name it early, it is an explicit "must" most candidates miss.
- Position the GTBank environment as the "comparable enterprise-grade environment" the JD asks for — a regulated bank's infrastructure is every bit as demanding as a telecom's IT estate.
- Frame Virk Cloud (a self-built Kubernetes PaaS on bare metal) as proof he architects infrastructure from first principles, not just operates it.

### On the gaps
- Be honest and specific on the networking-domain and cert gaps rather than glossing them — at architect level, credibility is the currency. Position CCNA and TOGAF as in-progress if he intends to pursue them.

---

## D) Comp and Demand

| Item | Data | Source |
|------|------|--------|
| Stated comp | Not disclosed | LinkedIn posting |
| Company | Telecel Ghana — formerly Vodafone Ghana; Telecel Group bought Vodafone's 70% for ~$900M (2023); Ghana govt holds 30% | Capacity / Connecting Africa / Ecofin |
| Restructuring / layoffs | Telecel explicitly stated "no plans to lay off anybody" post-acquisition | Ecofin Agency |
| Comp expectation | Architect-level role at a major, well-capitalized telecom — at or near the top of the Ghana enterprise-IT pay band. Telecom + post-acquisition modernization budget supports a competitive local package. | Profile guidance + company scale |

**Reading:** Per Oswald's profile, Ghana-based roles are evaluated on role quality, growth, and stack rather than a hard comp score. On those terms this is strong: a major, well-capitalized telecom (Telecel Group, pan-African), an architect title, and a modernization mandate (post-acquisition infrastructure rebuild) that means real, interesting work. Comp should be competitive for the Ghana market.

**Demand:** Infrastructure architect roles at large Ghanaian enterprises are steady. The post-acquisition modernization context means this is a build-and-improve role, not a maintain-only one — a positive.

---

## E) Customization Plan

### CV changes (Top 5)

| # | Section | Current | Proposed change | Why |
|---|---------|---------|-----------------|-----|
| 1 | Summary | "Platform engineer and solutions architect..." | "Infrastructure architect with 6 years designing and operating enterprise-grade on-prem + multi-cloud estates — AWS, GCP, Azure, OCI — across data centers, Kubernetes, networks, and DR." | Mirror the JD's "On-Prem and Cloud IT Infrastructure" framing |
| 2 | Four-cloud fluency | Listed in skills | Pull AWS + GCP + Azure + OCI into the summary and the first competency — it is an explicit "must" and a differentiator | Direct hit on the hardest "must" |
| 3 | Certs | Oracle certs mid-list | Foreground the 3 Oracle Cloud certs + AWS cert — they answer "Cloud certification required" and back the OCI "must" | Recruiter cert-screen |
| 4 | DR / HA / data centers | Spread across bullets | Group a clear infrastructure-architecture line: Tier III data centers, multi-cloud DR (AWS→GCP), HA K8s at 99.97% uptime | The JD weights DR/HA and data centers heavily |
| 5 | Architecture governance | Implicit | Add explicit "defined and enforced standards, ran architecture reviews" language to the Lead/CTO roles | The JD is governance-heavy (standards, reviews, approvals) |

### LinkedIn changes (Top 5)
1. Headline: "IT Infrastructure Architect | Multi-cloud (AWS/GCP/Azure/OCI) | Data centers, Kubernetes, DR"
2. About: lead with enterprise infrastructure architecture + four-cloud fluency
3. Featured: pin Virk Cloud (self-built Kubernetes PaaS)
4. Skills: pin Infrastructure Architecture, Multi-Cloud, Kubernetes, Terraform, Disaster Recovery, Data Center
5. Open-to-work: add "Infrastructure Architect", "Cloud Architect", "Solutions Architect" — Accra

---

## F) Interview Plan (STAR+R)

| # | JD Requirement | Story | S | T | A | R | Reflection |
|---|----------------|-------|---|---|---|---|-----------|
| 1 | Architect highly available infrastructure | GTBank HA Kubernetes | Bank needed reliable infrastructure for internal apps at scale | Architect HA clusters across on-prem environments | Designed multi-environment K8s with auto-scaling and self-healing | 3M+ daily requests at 99.97% measured uptime | Availability is an architecture property, not an ops afterthought — you design the failure modes in. |
| 2 | Multi-cloud (AWS/GCP/Azure/OCI) | Multi-cloud estate at GTBank + MyHealthCop | Workloads spanning AWS, Azure, GCP, on-prem | Architect and operate across providers | AWS + Azure at GTBank (VPC links to on-prem); AWS + GCP at MyHealthCop; OCI via Oracle-certified work | Coherent multi-cloud operations with cost control | Multi-cloud is a governance problem more than a technical one — without standards it becomes four silos. |
| 3 | Disaster recovery + high availability strategy | MyHealthCop DR design | Healthtech platform needed resilience against region failure | Design a DR strategy | Mirrored the AWS production environment on GCP — GKE, Cloud SQL, dual-environment CI/CD, secure VPCs | A tested, rapid-failover DR posture across two clouds | A DR plan you have not rehearsed is a hypothesis, not a strategy. |
| 4 | Infrastructure automation & DevOps | Founded GTBank's DevOps practice | Bank had manual, multi-day infrastructure processes | Automate and standardize | Terraform, Ansible, FluxCD GitOps; automated 95% of config management | Multi-day processes became reproducible deployments in minutes; deploy time down ~90% | Automation's real payoff is reproducibility and audit, not just speed — especially in a regulated estate. |
| 5 | Architect infrastructure from first principles | Virk Cloud — Kubernetes PaaS | No platform for startups to self-deploy with built-in observability | Architect and build a PaaS on bare metal | Designed the platform on RKE2, FluxCD, Terraform; provision the hardware and network myself | A production PaaS with instant cluster deployment | Building infrastructure end to end — hardware up — teaches you which abstractions actually hold under load. |
| 6 | Capacity planning, performance, lifecycle | Core banking on TKG | Core banking under continuous transaction load | Keep it scaled and performant | Capacity dashboards, threshold-based alerting for proactive scaling, lifecycle patching across 800+ pods | Sustained 1.5M+ daily transactions | Capacity planning is reading trend lines early — the worst time to scale is when the alert already fired. |
| 7 | Architecture standards & governance | Set engineering standards as founding CTO | 12-person team, no architecture standards | Define and enforce them | Set architecture, review norms, security scanning gates, CI/CD standards | A consistent, auditable engineering practice | Standards land when they are reviewed collaboratively, not decreed — governance is a forum, not a gate. |

### Case study to lead with
**Virk Cloud** — architecting a Kubernetes PaaS on bare metal, hardware up, is the cleanest proof of infrastructure architecture from first principles. Pair with **GTBank multi-cloud + DR** for the enterprise-scale dimension.

### Red-flag questions and answers
- **"You have no telecom experience."** → "Correct — my enterprise-grade environment has been banking. A regulated bank's IT estate has the same demands as a telecom's: data centers, multi-cloud, HA, DR, security, scale. The IT infrastructure architecture transfers directly; the telecom-specific context I'd ramp on fast."
- **"Cisco / CISSP / TOGAF?"** → Be honest: "I don't hold those. What I hold is four-cloud fluency with AWS and Oracle cloud certifications, and six years architecting enterprise infrastructure. CCNA and TOGAF are credentials I'd pursue — TOGAF I'm already planning to study. I'd rather be upfront than overclaim."
- **"How deep is your networking?"** → "Cloud networking is a strength — VPC design, private links to on-prem, WAF, load balancing. Classic SD-WAN and physical-firewall depth is lighter; I'd treat that as a fast ramp, not a claimed expertise."
- **"Why leave the bank?"** → The architect title and a modernization mandate — designing a telecom's infrastructure estate from a post-acquisition reset is the kind of greenfield-at-scale work he wants.

---

## G) Posting Legitimacy

**Assessment: High Confidence** — Real, active, and backed by a clear business rationale.

| Signal | Finding | Weight |
|--------|---------|--------|
| Posting freshness | 2 weeks old; "Be among the first 25 applicants" | Positive |
| Apply path | LinkedIn Apply button active | Positive |
| Company | Telecel Ghana — major telecom, formerly Vodafone Ghana, acquired by Telecel Group for ~$900M | Strongly positive |
| Business rationale | Post-acquisition modernization — a major telecom rebuilding its infrastructure genuinely needs an infrastructure architect | Strongly positive |
| Layoff signals | Telecel publicly stated no layoff plans after the acquisition | Positive |
| JD specificity | Detailed responsibilities, specific tech stack, specific cert list, clear role purpose | Positive |
| Reposting pattern | A near-identical "IT Infrastructure Architect at Telecel Ghana" was also posted ~5 days ago (job 4415031115) | Neutral-to-mild-concern |

**Context notes:** The duplicate posting (this one at 2 weeks, another at 5 days) is the only thing worth a second look. The most likely explanations are benign: two headcount on a team being built out post-acquisition, or a funnel-broadening repost. Telecel Ghana is unambiguously a real, large, well-capitalized company actively modernizing — not a profile that fits a ghost posting. Treat the duplicate as worth a question ("is this one role or two?"), not a red flag.

---

## Keywords extracted (ATS)

IT Infrastructure Architect · Cloud Architecture · AWS · GCP · Azure · OCI · Multi-Cloud · Data Center · Kubernetes · Virtualization · VMware · Disaster Recovery · High Availability · Terraform · Ansible · CI/CD · Infrastructure Automation · Capacity Planning · IAM · Architecture Governance · Enterprise Architecture · Networking · Telecom

---

## Recommendation

**Score 4.1/5 — Good match, worth applying. The strongest fit of the recent batch.**

This is the role that actually sits in Oswald's lane. IT Infrastructure Architect *is* his primary archetype, made explicit and elevated to architect level. It is the first of the recent four where he **meets the stated tenure** (6 years vs 5+), and he **hits the hardest "must"** — AWS + GCP + Azure + OCI fluency, with three Oracle certs backing the OCI requirement, which most candidates simply cannot. IaC/DevOps automation and DR/HA — both heavily weighted in the JD — are his core strengths. It is in Accra, his city, at a major, stable, well-capitalized employer with a genuine modernization mandate.

The honest gaps: no telecom-specific experience (softened — the JD accepts "comparable enterprise-grade environment", and banking clearly qualifies), lighter classic-networking depth (LAN/WAN/SD-WAN vs his cloud-native networking), and three certs he doesn't hold (Cisco, CISSP, TOGAF — softened by the JD's "or equivalent industry experience"). None is a hard blocker; the networking-domain gap is the one to be honest about in interviews.

**Recommendation:** Apply, and apply with confidence — this is his lane. Lead the application with four-cloud fluency, the GTBank enterprise-scale infrastructure record, and Virk Cloud as proof of architecture from first principles. Be straight about the networking and cert gaps rather than glossing them. A referral would help (the JD notes 2x interview odds). If he is serious, framing CCNA and TOGAF as in-progress would strengthen the cert story.

**Next actions:**
1. PDF generated — infrastructure-architect framing, four-cloud fluency foregrounded.
2. If applying: a short cover letter that names the four-cloud "must" hit, frames banking as the comparable enterprise environment, and is honest on networking/certs.
3. Ask, early in the process, whether the duplicate posting means one role or two.
