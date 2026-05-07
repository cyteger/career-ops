<!-- career-ops:render format=letter language=en company="google" date=2026-05-06 number=010 -->
# Oswald Gyabaah

**Site Reliability Engineer — Production Kubernetes, Multi-Cloud, Bank-Scale Systems**

+233 55 413 4307 | oswald.gyabaah@gmail.com | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana — open to US relocation (H-1B sponsorship)

---

## Professional Summary

Site Reliability Engineer running on-prem core banking on Tanzu Kubernetes Grid sustaining 1.5M+ daily transactions across 800+ production pods at 99.97% uptime, inside the Bank of Ghana regulatory perimeter. Systems-and-software hybrid in the literal sense — operate Kubernetes at scale and ship Python/Django + Next.js production services into the same environment, at the same employer, this year. Founded Guaranty Trust Bank Ghana's DevOps practice from zero and architected multi-cloud disaster recovery (AWS primary + GCP secondary) at MyHealthCop as founding CTO. Full SRE pillar coverage with numbers: reliability (99.97% uptime on 3M+ daily requests), latency (90% peak reduction via Redis + PostgreSQL tuning), performance, capacity (cluster sizing through 3x growth without capacity-driven incidents). Multi-cloud breadth across AWS, GCP, Azure, OCI; multi-distribution Kubernetes across EKS, GKE, TKG, RKE2.

---

## Core Competencies

- Distributed systems at scale (1.5M+ TPS, 800+ production pods)
- Reliability engineering — 99.97% uptime on 3M+ daily requests
- Latency, performance, capacity planning across production K8s
- Multi-cloud architecture and disaster recovery (AWS, GCP, Azure, OCI)
- Kubernetes mastery across EKS, GKE, TKG, RKE2
- Observability and incident response (Prometheus, Grafana, ELK, Sentry)
- Operations as software — IaC, GitOps, automated security gates
- Linux internals, on-call, root-cause analysis, post-incident review

---

## Technical Skills

- **Distributed Systems & Kubernetes:** Kubernetes across EKS, GKE, TKG/Tanzu, RKE2 (4 distributions in production); 800+ pod cluster ops; HA cluster topology; capacity planning through 3x growth; auto-scaling and self-healing; Helm; Istio Service Mesh with mTLS
- **Reliability & Observability:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry — dashboards, threshold alerting, structured logging, root-cause analysis, post-incident review, on-call experience
- **Languages & Systems:** Python (Django, FastAPI, Celery), Bash, JavaScript, TypeScript, Node.js — Linux internals, shell scripting, sysadmin tooling against live production servers
- **Cloud & IaC:** AWS (EKS, ECS, Lambda, S3, SQS/SNS, EventBridge, DynamoDB, VPC, IAM), GCP (GKE, Cloud SQL, Cloud Storage), Azure, OCI, VMware, on-prem bare metal — Terraform, Ansible, FluxCD, ArgoCD, Azure DevOps, GitHub Actions, Jenkins
- **Security & Networking:** IAM, OAuth2/Keycloak, OIDC, JWT, mTLS via Istio, Veracode, Trivy, audit-grade structured logging via Filebeat, Bank of Ghana regulatory perimeter
- **Integration & Messaging:** REST APIs, GraphQL, WebSockets, Kafka, RabbitMQ, AWS SQS/SNS, EventBridge — high-throughput background processing (1M+ daily jobs)
- **Databases:** PostgreSQL (query tuning, indexing, replication), MySQL, MongoDB, Firebase/Firestore, DynamoDB (single-table and multi-table), Convex, Redis
- **AI & Automation:** AI agents for sysadmin operations on live Linux production servers; LLM API integration (Claude, OpenAI), RAG, multi-agent orchestration, tool-use patterns
- **Leadership:** Founded 4-person DevOps team and 12-person cross-functional team; design reviews, code reviews, mentorship, on-call rotation

---

## Professional Certifications

- Oracle Certified DevOps Professional (Oracle), Aug 2025
- Oracle Certified Architect Associate (Oracle), Aug 2025
- Oracle Certified Foundations Associate (Oracle), Jul 2025
- AWS Certified Cloud Practitioner (AWS), May 2024
- AI Engineering Specialization (ByteByteAI), Mar 2026

---

## Professional Experience

### Core Banking Services Lead
**Guaranty Trust Bank Ghana LTD** | May 2025 - Present | Accra, Ghana

- Run on-prem Finacle core banking on Tanzu Kubernetes Grid sustaining 1.5M+ daily transactions across 800+ production pods at 99.97% uptime — own reliability, latency, performance, capacity end-to-end inside the Bank of Ghana regulatory perimeter.
- Lead L2 support operations correlating logs across internal apps and core banking microservices via the Elastic Stack — root-cause analysis, post-incident review, runbook updates, on-call rotation.
- Built Finacle-specific observability dashboards in Prometheus, Grafana, and the Elastic Stack with threshold-based alerting tuned for transaction-volume and response-time anomalies; structured Filebeat→Elasticsearch logging for audit.
- Architected integrations between Finacle core banking and multiple third-party systems (transaction portals, internal tools), with audit-grade structured logging.
- Built bank-wide OTP service (Django + Next.js) for 600+ internal users and a national ID verification service (Django + Next.js + self-hosted MinIO) — production code shipped into the same environment I operate.

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 - Present | Accra, Ghana

- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests at 99.97% measured uptime including scheduled maintenance.
- Founded the bank's DevOps team of 4 engineers from zero — designed the practice end-to-end (Git workflows, GitOps with FluxCD, declarative Helm config, security gates with Veracode + Trivy, runbooks, on-call rotation).
- Capacity planning through 3x request growth (1M to 3M+ daily) with no capacity-driven incidents — trended request volumes against pod headroom in Prometheus, modeled growth, designed HPA thresholds and node-pool sizing.
- Automated 95% of infrastructure configuration management via Terraform, Ansible, Python, and Bash — turning multi-day manual processes into reproducible, version-controlled deployments. Operations treated as software.
- Implemented CI/CD pipelines on GitHub Actions and Azure DevOps that cut deployment time by ~90% and increased release velocity ~5x; embedded Veracode + Trivy as automated security gates.
- Introduced a unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting with structured runbook references.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Designed multi-cloud disaster recovery architecture: AWS primary on EKS and ECS with Lambda for event-driven workloads; GCP secondary on GKE with Cloud SQL and Cloud Storage; mirrored IAM policies; secure VPCs with peering; dual-environment CI/CD; regular failover drills with no DR-related downtime.
- Led performance optimizations reducing peak request latency by 90% via Redis caching layer for high-frequency reads, PostgreSQL query tuning and indexing on a 10M+ row table, and database-level connection pooling.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS with multi-provider failover.
- Automated application delivery and infrastructure provisioning via CI/CD pipelines on GitHub Actions and Terraform, making deployments repeatable, auditable, and reversible.
- Architected the platform end-to-end: requirements gathering, system design, database modeling, API development, three client applications (patient Flutter mobile, professional Flutter mobile, React admin web).
- Led a 12-person cross-functional team (frontend, backend, mobile, product, design, QA) through full Agile lifecycle including design reviews, code reviews, on-call rotation, and stakeholder alignment.

---

## Projects

### Virk Cloud (virk.cloud) — Production K8s PaaS
**Founder & CTO** | Aug 2025 - Present

- Architect and operate a production Platform-as-a-Service on bare-metal VPS clusters with RKE2 Kubernetes — own cluster lifecycle, networking, observability (Prometheus + Grafana), GitOps with FluxCD, Terraform IaC, and developer-facing self-service workflows.
- Built management console (Next.js + Convex) for workload management, custom domains, monitoring dashboards — focused on developer experience and time-to-first-deploy.
- **Stack:** Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana, Next.js, TypeScript, Convex, Python, bare-metal Linux

### AI Agents for Infrastructure Operations
**Personal R&D** | 2024 - Present

- Build specialized AI agents for QA automation, code review, and sysadmin operations against live Linux production servers with real workloads — extending the "operations as a software problem" ethos to AI-driven sysadmin.
- Multi-agent orchestration, tool-use patterns, sandboxed execution, structured logging, prompt frameworks with output schema validation.
- **Stack:** Claude API, OpenAI API, Python, Linux production servers, AWS Lambda, EventBridge, DynamoDB

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
