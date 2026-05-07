<!-- career-ops:render format=a4 language=en company="mastercard" date=2026-05-06 number=009 -->
# Oswald Gyabaah

**Lead Platform Engineer — Multi-Cloud, Kubernetes, MLOps, AI Agents**

+233 55 413 4307 | oswald.gyabaah@gmail.com | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana — open to Singapore relocation

---

## Professional Summary

Lead-track platform engineer running on-prem core banking on Tanzu Kubernetes Grid sustaining 1.5M+ daily transactions inside the Bank of Ghana regulatory perimeter. Founded Guaranty Trust Bank Ghana's DevOps practice from zero, designing GitOps-native delivery with FluxCD, declarative Helm config, and embedded Veracode/Trivy security gates. Multi-cloud breadth across AWS, GCP, Azure, OCI, VMware, and on-prem bare metal; multi-distribution Kubernetes across EKS, GKE, TKG, and RKE2. Currently shipping production AI agent systems on the side — Palsar (Claude API monitoring SaaS), career-ops (multi-mode prompt orchestration framework with RAG retrieval and structured outputs), and R&D agents on live Linux infrastructure. Founded Virk Cloud, a self-service PaaS / internal developer platform with built-in CI/CD, observability, and log streaming. Strong Python and Bash; deep Terraform + GitHub Actions + Prometheus/Grafana/ELK fluency.

---

## Core Competencies

- Platform engineering at bank scale (1.5M+ TPS, 99.97% uptime)
- Multi-cloud architecture (AWS, Azure, GCP, OCI)
- Kubernetes mastery across EKS, AKS-adjacent, GKE, TKG, RKE2
- Infrastructure as Code (Terraform) and GitOps (FluxCD, ArgoCD)
- CI/CD pipeline design (GitHub Actions, Azure DevOps, Jenkins)
- Observability and ML-workload tuning (Prometheus, Grafana, ELK, Sentry)
- MLOps adjacency — AI agents, RAG, multi-agent orchestration, LLM-backed APIs
- Internal developer platforms and self-service automation (Virk Cloud PaaS)

---

## Technical Skills

- **Cloud & Containers:** AWS (EKS, ECS, Lambda, S3, SQS/SNS, EventBridge, DynamoDB, VPC), GCP (GKE, Cloud SQL, Cloud Storage), Azure, OCI, VMware vSphere, on-prem bare metal — Kubernetes across EKS, GKE, TKG/Tanzu, RKE2, AKS-adjacent (Azure DevOps fluent); Docker, Helm, Istio Service Mesh with mTLS
- **IaC, GitOps & CI/CD:** Terraform, Ansible, GitHub Actions, FluxCD, ArgoCD, Azure DevOps, Codemagic, Jenkins — declarative cluster config, multi-environment pipelines, artifact management, deployment strategies (blue/green, canary)
- **Observability:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry — dashboards, threshold alerting, structured logging, root-cause analysis
- **AI & MLOps Adjacency:** LLM API integration (Claude, OpenAI, Grok), Retrieval-Augmented Generation (RAG), AI agents, multi-agent orchestration, tool-use patterns, prompt frameworks with structured outputs, LLM-backed APIs and MCP-server-style architectures
- **Languages:** Python (Django, FastAPI, Celery), Bash, JavaScript, TypeScript, Node.js (Express)
- **Security & Networking:** IAM, OAuth2/Keycloak, OIDC, JWT, mTLS via Istio, Veracode, Trivy, audit-grade structured logging via Filebeat, Bank of Ghana regulatory perimeter
- **Integration & APIs:** REST APIs, GraphQL, WebSockets, Kafka, RabbitMQ, AWS SQS/SNS, EventBridge
- **Databases:** PostgreSQL, MySQL, MongoDB, Firebase/Firestore, DynamoDB, Convex, SQLite, Redis
- **Leadership:** Founded 4-person DevOps team and 12-person cross-functional team; technical project management, mentorship, ambiguous-goals execution

---

## Professional Certifications

- Oracle Certified Architect Associate (Oracle), Aug 2025
- AI Engineering Specialization (ByteByteAI), Mar 2026
- Oracle Certified DevOps Professional (Oracle), Aug 2025
- Oracle Certified Foundations Associate (Oracle), Jul 2025
- AWS Certified Cloud Practitioner (AWS), May 2024

---

## Professional Experience

### Core Banking Services Lead
**Guaranty Trust Bank Ghana LTD** | May 2025 - Present | Accra, Ghana

- Run on-prem core banking on Tanzu Kubernetes Grid sustaining 1.5M+ daily transactions across 800+ production pods inside the Bank of Ghana regulatory perimeter — own deployments, patching, incident response, capacity planning.
- Built Finacle-specific observability dashboards in Prometheus, Grafana, and the Elastic Stack (Elasticsearch, Logstash, Kibana, Filebeat) with threshold-based alerting tuned for transaction-volume and response-time anomalies.
- Architected integrations between Finacle core banking and multiple third-party systems (transaction portals, internal tools), with audit-grade structured logging to Elasticsearch via Filebeat.
- Lead L2 support operations correlating logs across internal apps and core banking microservices via the Elastic Stack for root-cause analysis and remediation.
- Built a bank-wide OTP service (Django + Next.js) integrating SMS and email gateways for 600+ internal users; built a national ID verification service (Django + Next.js) with self-hosted MinIO and automated verification workflows.
- Use AI agents and prompt-engineered workflows to accelerate L2 incident triage and migration test design — coordinated 10,000+ test cases across 13 modules during the Basis-to-Finacle migration cutover.

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 - Present | Accra, Ghana

- Founded the bank's DevOps team of 4 engineers from zero, replacing manual code handoffs with enforced Git workflows, containerized Kubernetes deployments, and automated release pipelines.
- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests at 99.97% measured uptime.
- Implemented Infrastructure as Code with Terraform and configuration management with Ansible, automating 95% of infrastructure work and turning multi-day manual processes into reproducible, version-controlled deployments.
- Introduced GitOps with FluxCD and declarative Helm-based cluster configuration for consistency, idempotency, and rapid disaster recovery rebuilds.
- Embedded Veracode and Trivy scanning into release pipelines as automated security gates; integrated security and compliance into the SDLC by default.
- Built CI/CD pipelines on GitHub Actions and Azure DevOps that cut deployment time by ~90% and increased release velocity ~5x.
- Managed multi-cloud infrastructure across Azure and AWS: resource provisioning, private VPC peering to on-prem systems, IAM, access control, and cost optimization.
- Introduced a unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Designed multi-cloud architecture: AWS primary on EKS and ECS with Lambda for event-driven workloads; GCP disaster recovery on GKE with Cloud SQL and Cloud Storage; mirrored IAM policies; secure VPCs with peering; dual-environment CI/CD for rapid failover.
- Automated application delivery and infrastructure provisioning via CI/CD pipelines on GitHub Actions and Terraform, making deployments repeatable, auditable, and reversible.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS with multi-provider failover.
- Led performance optimizations that reduced peak request latency by 90% through Redis caching, query tuning, and indexing in PostgreSQL.
- Architected the platform end-to-end across requirements gathering, system design, database modeling, API development; delivered three applications (patient-facing Flutter mobile, professional Flutter mobile, React admin web).
- Led a 12-person cross-functional team (frontend, backend, mobile, product, design, QA) through the full Agile lifecycle; sprint planning, design reviews, stakeholder management, hiring, and budget oversight.

---

## Projects

### Virk Cloud (virk.cloud) — PaaS / Internal Developer Platform
**Founder & CTO** | Aug 2025 - Present

- Architected a self-service Platform-as-a-Service for startups with built-in CI/CD, observability, and log streaming on bare-metal VPS clusters with RKE2 Kubernetes.
- Built a management console (Next.js + Convex) for workload management, custom domains, monitoring dashboards — focused on developer experience and time-to-first-deploy.
- Manage underlying infrastructure including cluster deployment, hardware and network provisioning, FluxCD GitOps, Terraform IaC, Prometheus/Grafana observability.
- **Stack:** Next.js, TypeScript, Convex, Tailwind CSS, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana, Python

### AI Agents for Infrastructure Operations & career-ops Prompt Orchestration
**Personal R&D** | 2024 - Present

- Build career-ops, a multi-mode prompt orchestration framework with explicit system-prompt and user-context separation, RAG retrieval over local knowledge bases, structured output schemas, version-controlled prompt library — used daily and applied to evaluate this Mastercard Foundry role.
- Build specialized AI agents for QA automation, code review, and sysadmin operations against live Linux production servers — multi-agent orchestration, tool-use patterns, sandboxed execution, structured logging.
- Patterns covered: RAG retrieval, multi-agent orchestration, tool-use, structured outputs, prompt evaluation, model-version pinning, prompt caching for cost control. Framework-equivalent to LangChain / LlamaIndex patterns implemented as a custom orchestration layer for explicit control.
- **Stack:** Claude API, OpenAI API, Python, Node.js, RAG patterns, multi-agent orchestration, AWS Lambda, EventBridge, DynamoDB, MCP-style tool-use

### Palsar — AI-Powered Monitoring SaaS (Claude API)
**Founder** | 2024 - Present

- Designed prompt-engineered workflows producing structured outputs at scale — explicit output schemas, few-shot examples, retry-on-malformed-output logic, model-version pinning, prompt caching for cost control.
- **Stack:** Next.js, TypeScript, Convex, Claude API, prompt caching, structured outputs

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
