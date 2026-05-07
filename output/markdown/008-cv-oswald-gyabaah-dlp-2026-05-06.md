<!-- career-ops:render format=a4 language=en company="dlp" date=2026-05-06 number=008 -->
# Oswald Gyabaah

**AI Engineer & Infrastructure Builder — LLM Agents, RAG, Production Systems**

+233 55 413 4307 | oswald.gyabaah@gmail.com | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

AI engineer and infrastructure builder shipping production LLM systems and treating prompt engineering as a primary craft. Build and maintain multi-mode prompt frameworks with explicit system-prompt and user-context separation, RAG retrieval over local knowledge bases, few-shot scoring rubrics, and multi-agent orchestration with tool-use. Production AI work includes Palsar (Claude API monitoring SaaS), Root-ID (AI agent identity platform), career-ops (multi-mode prompt pipeline used to evaluate this role), and live R&D agents on Linux production servers. Founded Guaranty Trust Bank Ghana's DevOps practice from zero and led 12-person cross-functional teams as founding CTO of MyHealthCop, shipping the assess-tailor-measure training loop across non-engineering roles. Python depth across Django, FastAPI, Celery; deep Kubernetes and multi-cloud operations.

---

## Core Competencies

- Prompt engineering — Chain-of-Thought, few-shot, RAG
- Multi-agent orchestration and tool-use patterns
- LLM API integration (Claude, OpenAI, Grok)
- Prompt frameworks, templates, and shared prompt libraries
- AI use case discovery and cross-functional facilitation
- Training and upskilling — assess, tailor, measure
- Python automation (Django, FastAPI, Celery)
- Production AI systems with structured outputs and observability

---

## Technical Skills

- **AI & Prompt Engineering:** LLM API integration (Claude, OpenAI, Grok), prompt engineering (Chain-of-Thought, few-shot, RAG), multi-agent orchestration, tool-use patterns, prompt frameworks and shared libraries, structured outputs and prompt evaluation, agent design for QA and sysadmin operations
- **Languages:** Python (Django, FastAPI, Celery), JavaScript, TypeScript, Bash, Node.js (Express)
- **Frontend:** React.js, Next.js, Tailwind CSS, Flutter
- **Cloud & Infrastructure:** AWS (EKS, ECS, Lambda, S3, SQS/SNS, EventBridge, DynamoDB, VPC), GCP (GKE, Cloud SQL), Azure, OCI, on-prem bare metal
- **Containers & Platforms:** Docker, Kubernetes (EKS, GKE, TKG/Tanzu, RKE2), Helm, FluxCD, ArgoCD
- **Integration & APIs:** REST APIs, GraphQL, WebSockets, Kafka, RabbitMQ, AWS SQS/SNS, EventBridge, SMS and email gateways, payment provider integrations
- **Databases:** PostgreSQL, MySQL, MongoDB, Firebase/Firestore, DynamoDB, Convex, SQLite, Redis
- **Observability & CI/CD:** Prometheus, Grafana, ELK Stack, Sentry, Terraform, Ansible, GitHub Actions, Azure DevOps
- **Leadership:** Cross-functional team leadership (12+), team founding from zero, training and upskilling, stakeholder management, technical project management

---

## Professional Certifications

- AI Engineering Specialization (ByteByteAI), Mar 2026
- Oracle Certified Architect Associate (Oracle), Aug 2025
- Oracle Certified DevOps Professional (Oracle), Aug 2025
- Oracle Certified Foundations Associate (Oracle), Jul 2025
- AWS Certified Cloud Practitioner (AWS), May 2024
- Django Web Framework (Coursera), Dec 2022

---

## Professional Experience

### Core Banking Services Lead
**Guaranty Trust Bank Ghana LTD** | May 2025 - Present | Accra, Ghana

- Use AI agents and prompt-engineered workflows to accelerate L2 incident triage and migration test design — coordinated 10,000+ test cases across 13 core banking modules with AI-assisted documentation and runbook generation.
- Led a 5-person QA team through the Basis-to-Finacle migration cutover over a two-week window, designing and executing 10,000+ test cases across 13 modules and 33 internal applications — assessed each tester's baseline, tailored ramp-up paths, and measured outcomes daily.
- Own the on-prem Finacle core banking deployment on Tanzu Kubernetes Grid, managing deployments, patching, and incident response across 800+ production pods sustaining 1.5M+ daily transactions.
- Architected integrations between Finacle core banking and multiple third-party systems including transaction portals and internal tools, operating inside the Bank of Ghana regulatory perimeter.
- Built a bank-wide OTP service (Django + Next.js) integrating SMS and email gateways to secure core banking access for 600+ internal users, with structured logging to Elasticsearch via Filebeat for audit.
- Built a national ID verification service (Django + Next.js) processing and storing ID documents in self-hosted MinIO with automated verification workflows.
- Lead L2 support operations correlating logs across internal apps and core banking microservices via the Elastic Stack for root-cause analysis and remediation.

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 - Present | Accra, Ghana

- Founded the bank's DevOps team of 4 engineers from zero — assessed each engineer's baseline (Git, Linux, Kubernetes), designed tailored ramp-up paths to a shared GitOps-native end state, ran weekly knowledge-share sessions and pair-programming rotations. All 4 productive on Kubernetes within 90 days.
- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests at 99.97% measured uptime.
- Implemented CI/CD automation that cut deployment time by ~90% and increased release velocity ~5x; introduced GitOps with FluxCD for declarative, version-controlled cluster deployments.
- Embedded Veracode and Trivy scanning into release pipelines as automated security gates; introduced declarative cluster config for rapid disaster recovery rebuilds.
- Automated 95% of infrastructure configuration management using Terraform, Ansible, Python, and Bash, turning multi-day manual processes into reproducible, version-controlled deployments.
- Managed multi-cloud infrastructure across Azure and AWS: resource provisioning, private VPC peering to on-prem systems, IAM, access control, and cost optimization.
- Introduced a unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Led a 12-person cross-functional team across product, design, QA, mobile, frontend, and backend through the full Agile lifecycle — designed sprint planning and design reviews for mixed-technical literacy, ran onboarding sessions for non-engineering hires on technical workflows, translated business requirements into architecture decisions for non-developer stakeholders.
- Architected the myhealthcop.com platform end-to-end across requirements gathering, system design, database modeling, and API development, delivering three applications: a patient-facing Flutter mobile app, a Flutter app for health professionals, and a React admin web dashboard.
- Designed AWS infrastructure running containerized microservices on EKS and ECS alongside Lambda functions for event-driven workloads, with autoscaling, load balancing, and IAM-controlled inter-service communication.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS with multi-provider failover.
- Led performance optimizations that reduced peak request latency by 90% through Redis caching, query tuning, and indexing in PostgreSQL.
- Designed a disaster recovery strategy mirroring AWS production on GCP using GKE, Cloud SQL, and Cloud Storage with secure VPCs and IAM policies.
- Automated application delivery and infrastructure provisioning via CI/CD pipelines on GitHub Actions and Terraform, making deployments repeatable, auditable, and reversible.

---

## Projects

### AI Agents for Infrastructure Operations & career-ops Prompt Pipeline
**Personal R&D** | 2024 - Present

- Build and maintain career-ops, a multi-mode AI prompt pipeline used daily for job-search workflows — explicit system-prompt + user-context separation, per-mode contracts, few-shot scoring rubrics, RAG retrieval over local knowledge bases, structured outputs validated against schemas. Used to evaluate this DLP role and generate this CV.
- Build specialized AI agents for QA automation, code review, and sysadmin operations running against live Linux production servers with real workloads — designed prompt frameworks and multi-agent orchestration patterns with tool-use.
- Maintain a documented, versioned prompt library (modes/, batch prompts, agent skill files) with clear conventions for system-layer vs user-layer customization — the same separation pattern that scales to team-wide prompt libraries.
- Built AWS Lambda functions triggered by EventBridge to deliver notifications on codebase events; used DynamoDB for NoSQL data modeling with both single-table and multi-table design patterns.
- **Stack:** Claude API, OpenAI API, Python, Node.js, RAG patterns, multi-agent orchestration, AWS Lambda, EventBridge, DynamoDB

### Palsar — AI-Powered Monitoring SaaS
**Founder** | 2024 - Present

- Designed prompt-engineered workflows producing structured outputs at scale — explicit output schemas, few-shot examples calibrated to monitoring data patterns, retry-on-malformed-output logic, model-version pinning, prompt caching for cost control.
- Built downstream tool-use integrations triggered by LLM decisions; production AI monitoring system with stable structured outputs.
- **Stack:** Next.js, TypeScript, Convex, Claude API, prompt caching, structured outputs

### Virk Cloud (virk.cloud) — Platform-as-a-Service
**Founder & CTO** | Aug 2025 - Present

- Architected a Platform-as-a-Service for startups with built-in CI/CD, observability, and log streaming on bare-metal VPS clusters; built a management console for workload management, custom domains, and monitoring dashboards.
- **Stack:** Next.js, TypeScript, Convex, Tailwind CSS, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana, Python

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
