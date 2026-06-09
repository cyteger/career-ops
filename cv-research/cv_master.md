# Oswald Gyabaah

**DevOps/Platform Engineer | Solutions Architect**

oswald.gyabaah@gmail.com | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana | Open to remote

---

## Professional Summary

Platform and infrastructure engineer with 6 years (since graduating in 2020) building and operating systems on on-prem Kubernetes, AWS, and GCP. Owns the Finacle core banking platform at GTBank Ghana, fully containerized on Tanzu Kubernetes Grid behind 1.5M+ daily transactions, including the application-tier disaster recovery for 268 apps (RPO 0, 22-minute RTO achieved in live drills). Founded the bank's DevOps practice from scratch and serves as its bank-wide code-review approver. Also defines technical requirements, produces high-level designs, and owns UAT for cross-team application projects. Led and mentored 13 engineers across MyHealthCop and GTBank, interviewing every hire personally and moving juniors from general DevOps into core banking service management. Earlier, founding CTO of MyHealthCop, building the mobile, web, and backend platform end to end for a 12-person team. Currently building Lodestar, a live LLM-assisted resume product, and runs AI-agent experiments for infrastructure operations as a learning project.

---

## Experience

**DevOps/Platform Engineer and Core Banking Services Lead, GTBank Ghana** | Apr 2024 to Present | Accra, Ghana

Joined to found the bank's DevOps practice. Scope expanded in May 2025 to add ownership of the Finacle core banking platform while retaining DevOps leadership. Also serve as the bank-wide approver for code-related changes, and carry an add-on solution-architecture and technical-program responsibility for cross-team application delivery.

*Core banking platform (Finacle)*
- Own Finacle 11 in production, fully containerized on Tanzu Kubernetes Grid (TKG): 800+ pods serving 1.5M+ daily transactions across internet banking, mobile app, USSD, ATM, and POS channels.
- Maintain the internal integration layer between channels and Finacle: REST middleware, an in-house API gateway, and microservices for branches, accounts, transactions, cheques, and customers.
- Support the end-of-day batch cycle (around a 1-hour window) at the platform layer, troubleshooting long-running or stuck EOD runs by resolving resource exhaustion, pod-scaling problems, and throughput bottlenecks.
- Led the QA workstream for the Basis-to-Finacle core banking migration: 10,000+ test cases across 13 modules and 33 applications, then assumed platform operations after go-live.
- Ran the production cutover for 3,000,000+ accounts: planned for a 3-hour downtime window, completed in 2 hours, with no major data loss and only a few minor defects post-cutover.
- Built Finacle observability dashboards and alerting on Prometheus, Grafana, and the Elastic Stack, and perform L2 support and root-cause analysis.

*Payments and settlement rails (monitoring and integration maintenance)*
- Maintain and monitor the integration applications for the bank's payment rails so business users can post: GhIPSS, mobile money, card/ATM/POS via the Postilion switch, RTGS, ACH, SWIFT, OE PAY, and remittance providers (Remitly, Ria).
- First responder when a payment message fails to reach SWIFT or a downstream provider due to an integration or connectivity failure. Restore the integration path; business users own the posting itself.

*Disaster recovery and resilience*
- Own application-tier disaster recovery for 268 applications to a standby DR data center. Authored the DR policy and runbooks and lead bank-wide failover simulations involving 600+ staff.
- Achieved RPO 0 (database replication via Oracle Data Guard, owned by the DBA team and coordinated by me) and a 22-minute RTO in live failover drills, improved from 1 hour on the first run against a designed target of 45 minutes. No real disaster event has occurred.
- Designed the application-layer DR sync model across two independent, VMware-managed Kubernetes clusters (DC and DR), keeping app state in sync via Git and FluxCD.
- Run parallel Jenkins pipelines with selectable primary and DR targets, backed by Harbor image mirroring, and use Velero for cluster backups.

*DevOps practice (founding and platform standards)*
- Founded the DevOps team of 4 and personally interviewed every member. Mentored juniors from general DevOps into core banking service-management roles.
- Built the DevOps adoption roadmaps for both the application-development and application-support teams, plus git-driven standards, deployment runbooks, and Azure DevOps Server pipeline templates.
- Drove adoption across 2 teams (application development and application support/operations) covering roughly 40 applications under DevOps standards and CI/CD governance, of which 10 are migrated to Kubernetes so far and the rest are pending container-readiness.
- Reduced hands-on deploy effort per app by roughly 90% by replacing manual multi-step releases with a single GitOps reconcile (FluxCD, Helm, Azure DevOps Server).
- Built a platform deployment capability of one release every five minutes, around the clock (org-wide cadence is governed by multi-stakeholder change management).
- Run high-availability Kubernetes on-prem serving 3M+ daily requests, with most months measured at or above 99.9% via Prometheus and Gatus (no formal SLA), plus autoscaling and self-healing.
- Automated configuration management with Ansible, Python, and Bash, covering roughly 95% of managed configuration.

*Platform and security operations*
- Manage secrets with External Secrets Operator backed by HashiCorp Vault, keeping credentials out of Git in the FluxCD GitOps model.
- Run TLS/PKI on a public CA (Sectigo) with annual renewal and manual rotation; certificates are stored in Vault and loaded dynamically by apps such as Elasticsearch and Harbor.
- Deployed Istio solely to provide in-cluster mTLS between services (no traffic management, routing, or canary use).
- Manage StorageClasses and PVCs over network NFS (the sysadmin team owns the underlying NFS).
- Operate cluster networking on Antrea/NSX-T with NetworkPolicies for namespace segmentation, and expose services via Gateway API HTTPRoute on ingress controllers with MetalLB for bare-metal L4 load balancing.
- Handle delegated cluster authentication via vSphere (vsphere.local), with Keycloak and Active Directory for application login.
- Run Veracode and Trivy on all deployments and block every finding above medium severity before deploy (roughly 10-15 per app), patching first. Allow up to a 2-week deferral window for extensive fixes.
- Operate a unified observability stack (Prometheus, Grafana, the Elastic Stack with Filebeat, Sentry, and Gatus). Most outages are detected within 90 seconds; monthly incidents run 0-2 and typically resolve in minutes.
- Provision multi-cloud infrastructure on Azure and AWS with private VPC links and access control.

*Compliance and audit*
- Operate within PCI-DSS scope and an ISO 27001-certified environment, supporting internal and external audits with the controls I own: credential segregation, incident runbooks, change management, and the bank-wide code review and approval gate.
- Meet Bank of Ghana requirements: in-country data residency, primary DC on bank premises, and a DR site 250+ km away under regulator-set RTO/RPO targets.
- Built and run the bank-wide OTP service (Next.js, Django) for 600+ users and the Ghana Card verification (KYC) service (Next.js, Django, MinIO).

*Solution architecture and technical-program work (add-on responsibility)*
- Gathered and wrote technical requirements for incoming application requests, produced high-level architecture, and recommended the design and coding approach. Recommendations were non-binding; development teams chose their own implementation.
- Owned UAT, validating delivered work with business users for sign-off.
- Delivered roughly 5 projects on time before handing the function over to focus on Finacle.
- Presented to developers, business users, and the group head, and occasionally to the CIO and CSO.

**Freelance DevOps Engineer, bandana.com** | Oct 2025 to Jan 2026 | Remote (US timezone)

- Provided freelance DevOps engineering for a US-based team, working US business hours (UTC-4/-5) in a remote, distributed workflow.

**Founding CTO, MyHealthCop** | Jan 2021 to Mar 2024 | Accra, Ghana

Built the company's product and platform end to end and led a 12-person cross-functional team. At handover the platform had roughly 1,000 users and 40+ health professionals, having just gone live with no downtime and beginning to scale.

- Built three applications: a patient app and a professional app (both Flutter) and a React admin console.
- Architected the AWS backend on EKS, ECS, and Lambda with autoscaling and load balancing.
- Designed background processing on SQS and SNS with multi-provider failover, built for scale ahead of demand.
- Cut p95 request latency by tuning Redis caching and PostgreSQL queries and indexes.
- Built CI/CD with GitHub Actions and Terraform, and a GCP disaster-recovery mirror on GKE, Cloud SQL, and Cloud Storage.

**National Service and Freelance Projects** | May 2020 to Jan 2021 | Accra, Ghana

- Completed mandatory Ghana national service alongside freelance software projects following graduation.

---

## Selected Projects

**Lodestar** (lodestar.cv), Founder | 2025 to Present | Live
- Live product that lets users build and manage resumes with integrated LLM review, reframing, and a feature that tailors a resume to a job description pulled from a URL, an uploaded file, or pasted text. A portfolio-site feature is planned.
- Stack: Next.js, Convex.

**Vistara**, Founder | 2026 to Present | Live
- Property tenant-assessment platform that lets renters evaluate housing conditions before signing a lease. Live and just launched: a landing site, a tenant web app, an admin dashboard, and a Flutter field app.
- Stack: Next.js, React, TypeScript, Flutter, Codemagic.

**Digital-Recon**, Founder | 2025 to Present | WIP (building)
- Real-time reconciliation engine, building now. Started in response to real reconciliation pain at GTBank: transactions stuck in ledgers, debits without matching credits and the reverse, and failed transfers not auto-reversed that needed manual intervention. Intended to evolve into a sidekick that handles what the core banking system does not.
- Stack: React, TypeScript, Python, Kafka, Celery, Elasticsearch, PostgreSQL, Docker.

**Virk Cloud**, Founder/CTO | 2025 to Present | WIP (building)
- Platform-as-a-service offering CI/CD, observability, and log streaming, building now. Currently the only environment where I run admission control and policy-as-code (not in use at the bank).
- Stack: Next.js, TypeScript, Convex, Tailwind CSS, RKE2, FluxCD, Terraform, Prometheus, Grafana, Python.

**AI Agents for Infrastructure Operations**, Personal R&D | 2024 to Present
- Learning and growth project (not production at the bank): QA, code-review, and sysadmin agents running on personal live Linux hosts, using RAG, tool-use, and multi-agent orchestration on AWS Lambda, EventBridge, and DynamoDB.

**Education Research and Innovation Foundry** (erifoundry.org), Founder | 2025 to Present
- Research project on adaptive learning, cognitive modeling, and educational analytics.

---

## Speaking and Writing

- Owner and author of the **risingEngineers** Substack, publishing engineering articles.
- MC and moderator at a Microsoft community event (2025).

---

## Technical Skills

- **Cloud and Infrastructure:** AWS (EKS, ECS, Lambda, S3, SQS/SNS, EventBridge, DynamoDB, VPC), GCP (GKE, Cloud SQL, Cloud Storage), Azure, OCI, VMware/vSphere, on-prem Tier III data centers
- **Containers and Orchestration:** Docker, Docker Compose, Kubernetes (TKG/Tanzu, EKS, GKE, RKE2), Helm, Istio (mTLS only), Antrea/NSX-T, MetalLB, Gateway API HTTPRoute
- **CI/CD and GitOps:** FluxCD, ArgoCD, Jenkins, GitHub Actions, Azure DevOps Server, Codemagic, Harbor, Terraform, Ansible
- **Platform and Security:** HashiCorp Vault, External Secrets Operator, Keycloak, Active Directory, Sectigo PKI/TLS, NetworkPolicies, Velero, NFS CSI (StorageClasses/PVCs), Veracode, Trivy
- **Observability:** Prometheus, Grafana, Elastic Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry, Gatus
- **Core Banking and Payments:** Finacle 11, EOD/BOD batch, REST middleware and API gateway, microservices integration, Oracle Data Guard (coordinated), GhIPSS, mobile money, card/ATM/POS (Postilion), RTGS, ACH, SWIFT (integration monitoring)
- **Backend and APIs:** Python (Django, FastAPI, Celery), Node.js (Express), REST, GraphQL, WebSockets
- **Frontend and Mobile:** JavaScript, TypeScript, React.js, Next.js, Tailwind CSS, Flutter
- **Databases:** PostgreSQL, MySQL, MongoDB, Firebase/Firestore, DynamoDB, Convex, SQLite, Redis
- **Messaging and Queues:** AWS SQS/SNS, EventBridge, RabbitMQ, Redis queues, Kafka
- **Testing:** Jest, React Testing Library, Cypress, Playwright, pytest, UAT coordination
- **AI and Agents:** LLM API integration (Claude, OpenAI, Grok), RAG, agent development, multi-agent orchestration, tool-use patterns
- **Languages and Scripting:** Python, Bash, SQL
- **Ways of Working:** Platform engineering, site reliability engineering (SRE), full project lifecycle (requirements through delivery), high availability, disaster recovery, incident management, infrastructure as code, Agile/Scrum, Kanban, stakeholder management, risk assessment, mentoring and team leadership

---

## Certifications

**Held**
- AI Engineering Specialization, ByteByteAI (Mar 2026)
- Oracle Certified DevOps Professional (Aug 2025)
- Oracle Certified Architect Associate (Aug 2025)
- Oracle Certified Foundations Associate (Jul 2025)
- AWS Certified Cloud Practitioner (May 2024)
- Django Web Framework, Coursera (Dec 2022)

**In Progress**
- Certified Kubernetes Administrator (CKA)
- Certified Kubernetes Security Specialist (CKS)
- AWS Certified Solutions Architect, Associate (SAA)
- AWS Certified Solutions Architect, Professional (SAP)
- Google Cybersecurity, Coursera

---

## Education

**BSc Computer Engineering, Ashesi University** | Sep 2016 to May 2020 | Berekuso, Ghana