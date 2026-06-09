# Master CV Gap Inventory — Oswald Gyabaah

Deduplicated and deconflicted across six expert lenses (platform/SRE, certifications, FANG-promo, core-banking domain, recruiter-screen, architect/leadership). Each item is tagged with the likelihood that he **already did this and just failed to document it** — not a suggestion to fabricate. `[high]` = almost certainly has it given his exact role/stack. `[medium]` = plausible, role-dependent. `[low]` = genuinely uncertain or a stretch; confirm before adding.

---

## 1. Skills & Tools (name the stack behind work already described)

These are mostly invisible operational layers that someone running self-hosted Kubernetes + Finacle at a regulated bank cannot avoid owning. The fix is naming the tool inside an existing bullet, not adding a new claim.

- **[high] Secrets management** — Sealed Secrets / External Secrets Operator / Vault / SOPS / cloud KMS. GitOps with FluxCD at a bank means secrets cannot sit in Git plaintext. First question any reviewer asks about a Git-based deploy model.
- **[high] Certificate management / PKI** — cert-manager, internal CA, Let's Encrypt, cert rotation, mTLS. On-prem bank with 268 apps, an OTP service, and Istio cannot run without managed TLS.
- **[high] Persistent storage / CSI for stateful workloads** — vSphere CSI (likely, since Tanzu), Longhorn, Ceph/Rook, NFS, plus StorageClass/PVC/PV management and MinIO operations. Finacle on TKG and self-hosted MinIO are stateful; the storage layer is never named.
- **[high] Backup & restore / DR tooling** — Velero, etcd snapshots, vSphere/array snapshots, DB-native backups, and a restore-test cadence. A 45-min RTO / near-zero RPO claim is unverifiable without this.
- **[high] Cluster networking / CNI** — Antrea/NSX-T (TKG default), Calico, or Cilium, plus NetworkPolicies to segment banking namespaces.
- **[high] Ingress & L4 load balancing on bare metal** — NGINX Ingress / Contour / Traefik for L7; MetalLB / F5 / HAProxy / NSX for L4. Exposing 268 apps + OTP service to 600+ users requires a deliberate layer. WAF in front?
- **[high] SSO / IAM / directory integration** — Active Directory / LDAP via OIDC, Keycloak / Dex / ADFS for cluster RBAC and app login. A bank with 600+ users does not run local accounts.
- **[high] Linux & networking fundamentals** — systemd, sysctl/kernel tuning, DNS, firewalls, VLANs, routing, data-center LBs. He runs bare metal in Tier III DCs and AI agents on live Linux prod; FANG infra screens test this hard.
- **[medium] Policy-as-code / admission control** — OPA Gatekeeper, Kyverno, Pod Security Standards (block unsigned images, require resource limits, restrict privileged pods). Natural adjacent to his existing Trivy/Veracode work.
- **[medium] Istio service mesh depth** — mTLS, retries/timeouts/circuit-breaking, weighted/canary traffic splitting, mesh telemetry. Currently a one-word keyword; substantiate or trim.
- **[medium] FinOps / Kubernetes cost tooling** — Kubecost / OpenCost, request-and-limit right-sizing, reserved capacity, idle reclaim, with a number. Currently just the phrase "cost optimization."
- **[medium] vSphere / ESXi administration & hardware ops** — bare-metal/VM provisioning, capacity planning, DR-site hardware bring-up. VMware appears only in the skills line, unsupported by any bullet.
- **[low] Go (Golang)** — operator/controller, admission webhook, Prometheus exporter, or CLI. Lingua franca of the K8s ecosystem and common on platform JDs; nothing in his stack forces it, so confirm rather than assume.

---

## 2. Certifications

- **[medium] TOGAF Foundation (in progress)** — actively self-studying for the architect pivot; appears nowhere. List honestly as in-progress with a target date. NEVER imply it is earned.
- **[high] Name the actual Oracle track precisely** — three Oracle certs in Jul–Aug 2025 almost certainly came from one structured program (likely OCI / VMware-Tanzu / Finacle-infra tied). Rename to the real credential (e.g. "Oracle Cloud Infrastructure 2025 Architect Associate") and surface any bundled modules he did not list.
- **[medium] Vendor/OEM training certificates from the bank** — VMware Tanzu enablement, Infosys/Finacle administration, Elastic, possibly Red Hat. Running Finacle on TKG almost always comes with vendor-delivered completion certs people omit as "internal."
- **[medium] Mandatory bank security/compliance training** — ISO 27001 awareness, PCI-DSS, infosec. Regulated banks usually mandate annual training that is citable.
- **[low] CKA (Certified Kubernetes Administrator)** — highest-ROI cert he does NOT hold; does CKA-level work daily. Pursue, do not claim.
- **[low] AWS Solutions Architect Associate** — only holds entry-level Cloud Practitioner despite years of real AWS architecture. Pursue next.
- **[low] HashiCorp Terraform Associate** — uses Terraform daily; cheap validation. Pursue.
- **[low] ITIL Foundation** — runs L2 support, incident/RCA, DR runbooks. Only relevant if targeting enterprise/MSP roles. Confirm if trained.
- **[low] Azure AZ-104 / AZ-305** — manages Azure + Azure DevOps but uncertified. Lower priority; depends on real Azure depth beyond pipelines.

---

## 3. Accomplishments & Metrics (mine real numbers; convert activities to outcomes)

- **[high] GTBank TPM / architecture role — ENTIRELY MISSING.** Single highest-value omission. A Technical Program Manager role with architecture responsibility supplies the cross-team coordination + system-design signal that Solutions Architect and Engineering Manager screens want first. Needs dates, teams/workstreams coordinated, architecture decisions owned vs recommended, on-time delivery record.
- **[high] MTTR / incident-volume reduction** — the DevOps bullet literally says "reducing mean time to resolution" with no number. Before/after detect+resolve time, monthly incident count, Sev1/Sev2 trend.
- **[high] SLA/SLO attainment + on-call load** — formal availability target, months/quarters held, pages-per-week then vs now. The 99.97% is currently a bare metric with no SLA framing.
- **[high] Cloud cost savings / on-prem & licensing avoidance** — percentage cut, VM/server consolidation count, commercial tools replaced with open source (e.g. VMware sockets). Even a rough annual figure or "avoided buying N servers."
- **[high] Compliance & audit outcomes** — PCI-DSS, ISO 27001, SWIFT CSP, Bank of Ghana IT exams, internal/external audit. Did his controls (scanning, Git workflows, access control, DR runbooks) help pass an audit or close findings? How many, under deadline?
- **[high] DR: achieved vs designed + real failover** — RTO/RPO actually hit in live drills (not just the 45-min target), improvement across tests, number of full drills, and any real outage where the runbooks were used in anger with recovery time/impact.
- **[high] Team growth & people development** — who he hired/interviewed, whether the 4-person DevOps team grew, juniors mentored who got promoted, total engineers managed/mentored across roles.
- **[high] Security posture outcomes** — CVEs/vulns caught/blocked after Veracode+Trivy, patch SLA, % of deployments through mandatory scanning, releases blocked on findings.
- **[high] Org-level DevOps adoption** — teams/developers across the bank that adopted his Git workflows + CI/CD, apps onboarded to Kubernetes/GitOps, deployment-frequency or lead-time change org-wide.
- **[high] MyHealthCop people + business outcomes** — hiring/mentoring depth, plus users (patients + professionals), payment/transaction volume, uptime delivered, funding/partnerships.
- **[medium] Scale as growth, not snapshot** — scaled from X to 1.5M daily txns; peak TPS on payday/holiday/national-event spikes the platform held. Same for the 3M+ daily requests.
- **[medium] Basis-to-Finacle cutover outcome** — accounts/data migrated, planned vs actual downtime window, defects caught pre-prod vs leaked, zero-data-loss status. (Promote the migration itself to a headline, QA leadership as one facet.)
- **[medium] AI agents — real usage** — are any agents actually used in GTBank ops, or pure R&D? Currently reads as resume-driven development with no adoption.

---

## 4. Banking / Fintech Domain (surface the ledger, not just the pods)

The single biggest pool of un-mined market value. A Finacle services lead in a Ghanaian bank almost certainly touched these; they were stripped for a generic DevOps CV. Keep as optional master blocks he subsets for banking/fintech targets (Ecobank, MoMo, payment processors); drop for generic remote-infra renders.

- **[high] GhIPSS rail integrations** — GIP instant pay, GhQR, gh-link, e-zwich. National switch; gold for local banking/fintech. Posting/settlement vs connectivity/host-to-host side?
- **[high] Mobile money integration** — MTN MoMo, Telecel Cash, AirtelTigo bank-to-wallet / wallet-to-bank into Finacle, plus reconciliation/callback handling. Dominant Ghana channel.
- **[high] End-of-day / beginning-of-day batch** — Finacle EOD/BOD window length, interest accrual, GL posting, account sweeps, troubleshooting a stuck/overrunning cycle. The heartbeat of core-banking ops.
- **[high] Oracle DB under Finacle** — RAC, Data Guard (almost certainly the near-zero-RPO mechanism), ASM, RMAN backups, log shipping, tuning. He holds Oracle certs and partnered on DR; the CV buries this as "the database team."
- **[high] Integration middleware / ESB / API gateway** — what actually sits between Finacle and channels: Finacle Connect/FIC, IBM IIB/ACE, MuleSoft, WSO2, Kong, or in-house; protocols (SOAP/REST, MQ, host-to-host files). Replaces the vaguest banking bullet on the CV.
- **[medium] ISO 8583 / card switch** — ATM/POS, Visa/Mastercard/gh-link, a switch (SmartVista, Postilion), stand-in processing, even on integration/monitoring side.
- **[medium] RTGS / ACH / SWIFT settlement** — Ghana RTGS/GISP large-value, ACH bulk clearing, SWIFT MT/MX and ISO 20022 migration, cutoff windows, gateway uptime.
- **[medium] HSM / key management / payment crypto** — Thales/nCipher, key ceremonies, PIN/MAC, TLS cert lifecycle for payment endpoints, even as a dependency.
- **[medium] Digital channels** — internet banking, mobile app, USSD short-code; whether his OTP/ID services secured customer channels or only internal staff.
- **[medium] Bank of Ghana regulatory exposure** — cybersecurity directive, data residency (kept DR site in-country?), regulator-set RTO/RPO, regulatory returns, incident-reporting timelines.
- **[medium] PCI-DSS scope + AML/KYC** — whether card data put the platform in PCI scope; whether the national-ID verification service feeds KYC/onboarding, sanctions/PEP screening, transaction monitoring.
- **[medium] Finacle product specifics** — version (10.x/11.x), modules (core, FEBA, Connect24, treasury), scripting/customization; his actual role in the Basis-to-Finacle data-migration mapping/config vs only QA.
- **[medium] Reconciliation pain at the bank** — whether Digital-Recon came from real GTBank recon problems (settlement breaks vs GhIPSS/MoMo/switch, suspense/GL clean-up) and at what volume. Ties the side project to real work.

---

## 5. Architecture & Leadership (separate senior engineer from architect)

- **[high] ADRs / design docs / written architecture artifacts** — write-ups of real trade-offs (TKG over OpenShift, FluxCD over ArgoCD, GCP for DR). How many, signed off above him? Architect screens want proof he thinks in architecture.
- **[high] Reference architectures / golden paths others adopted** — standard pipeline, cluster topology, observability baseline from founding the DevOps practice; how many teams/apps adopted them. Producing patterns others follow is THE architect signal.
- **[high] Security architecture** — IAM design, network segmentation, secrets strategy, audits passed at the bank. SA/EA bank roles weight this heavily.
- **[high] Executive / stakeholder presentations** — who he briefed during the migration and DR sims (CIO, CTO, steering committee, auditors, regulator); membership on any architecture review board or CAB. Top SA interview probe.
- **[medium] Vendor selection / RFP / TCO** — tool evaluations (Tanzu, Veracode, Harbor, gateways), POCs, build-vs-buy or cloud-vs-on-prem TCO presented to leadership, with the decision and impact.
- **[medium] Talks / writing / open-source footprint** — meetup/conference/brown-bag talks, blog posts, erifoundry research output, what is actually on github.com/cyteger (referenced in header but nothing points to it), any merged PR to a known project. Disproportionate leverage for a Ghana-based candidate chasing remote roles.
- **[low] TOGAF/ArchiMate applied to a real diagram/decision** — any concept applied to actual work, beyond reading the standard.

---

## 6. Framing (structure, not new claims)

- **[high] Master title too broad** — "Full-Stack Software and Infrastructure Engineer" signals generalist at a seniority that wants one clear discipline. Needs a neutral master anchor + swappable role-specific titles per target.
- **[high] Summary buries the strongest credential** — opens with filler ("at scale," "production systems") and only reaches Finacle/1.5M txns second. Lead with the unfakeable proof.
- **[high] Two concurrent "Present" GTBank Lead roles** — promotion, scope expansion, or two jobs? Ambiguity reads as inflation. Needs a progression marker or an explicit scope-expansion line.
- **[high] Founder-title stack** — CTO + 4 founder projects, four concurrent with a demanding bank job, reads "spread thin / nothing shipped" unless ranked by traction. Which have real users/deployments?
- **[high] Section order** — Skills currently sits above Experience and entry-level certs sit above the strongest work. Move to: Summary → Experience → Selected Projects → Skills → Certifications → Education.
- **[high] Skills list is a ~90-item keyword wall** — keep the full superset in the master file; every submitted subset must trim hard to ~12–15 target-relevant tools.
- **[medium] Round-number cluster** — 90% (twice), 95%, 99.97%, 5x with no baseline. Convert to auditable before/after ("deploys from ~2h to ~12min") or name the measurement source ("99.97% via Prometheus over N months").
- **[medium] Unexplained May 2020–Jan 2021 gap** — ~8 months after graduation. Likely Ghana national service / freelance / pre-incorporation MyHealthCop. Name it; may add a legitimate line.
- **[medium] Tenure framing** — "6 years" is accurate but flat; consider "6 years, including 2+ owning core banking infra and 3 as founding CTO." Confirm any paid work predating MyHealthCop. Resolve the 6-vs-5 mismatch between summary and profile notes; pick one defensible number for all subsets.
- **[medium] Remote/timezone signal invisible** — for international remote, add a one-line "Open to remote. Accra (GMT), strong EU and US-East overlap." Confirm distributed/cross-timezone experience.
- **[medium] ATS outcome keywords thin** — tool keywords are dense, but role/outcome phrases ATS filters search (site reliability, SLO/SLA, on-call, incident management, infrastructure as code, high availability, platform engineering) are missing where they are true.
- **[medium] Title vs memory mismatch** — CV says "Core Banking Services Lead"; memory notes "Manager, Finacle Services Team." Pick one consistent title; a recruiter cross-checking LinkedIn will flag it.

> Hygiene note: five lenses flagged a pasted "Lodestar" onboarding email at cv.md lines 131–136. The current file ends cleanly at line 129 with no such text — it has already been removed. No action needed; do not re-flag.
