<!-- career-ops:render format=a4 language=en company="uipath" date=2026-05-06 number=011 -->
# Oswald Gyabaah

**Forward Deployed Engineer — AI Agents, Enterprise Integration, Customer Delivery**

+233 55 413 4307 | oswald.gyabaah@gmail.com | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana — open to Bucharest relocation (EU Blue Card)

---

## Professional Summary

Engineer shipping AI agent systems and enterprise integrations into production environments. Build and maintain career-ops, a multi-mode prompt orchestration framework with system + user-context separation, RAG retrieval, multi-agent tool-use, structured outputs, and prompt evaluation rubrics — used daily and applied to evaluate this UiPath role itself. Architect bank-grade enterprise integration: Finacle core banking integrated with multiple third-party systems on Tanzu Kubernetes Grid sustaining 1.5M+ daily transactions inside the Bank of Ghana regulatory perimeter. Customer-adjacent technical leadership as founding CTO of MyHealthCop with a 12-person cross-functional team across product, design, mobile, frontend, backend, QA. Strong Python (Django, FastAPI, Celery) and TypeScript (Next.js, Node.js) production depth; deep API integration, REST/GraphQL, multi-cloud (AWS, GCP, Azure, OCI), Kubernetes ops at scale.

---

## Core Competencies

- Agentic automation and AI workflow design (career-ops, R&D agents on live infra)
- Prompt engineering — CoT, few-shot, RAG, tool-use, model tradeoffs (capability/latency/cost)
- LLM API integration (Claude, OpenAI, Grok) and structured-output prompt patterns
- Enterprise system integration (Finacle ↔ third-party, SMS/email gateways, payment providers)
- API and SDK development with Python, TypeScript, REST, GraphQL
- Customer-facing delivery and stakeholder alignment
- Cross-system debugging across AI inference, integration layers, observability
- Founded a 4-person DevOps team and a 12-person cross-functional team

---

## Technical Skills

- **AI & Agentic Automation:** Multi-mode prompt orchestration (career-ops), LLM API integration (Claude, OpenAI, Grok), Retrieval-Augmented Generation (RAG), multi-agent orchestration, tool-use patterns, structured outputs and prompt evaluation, MCP-style architectures, model selection by capability/latency/cost
- **Languages & APIs:** Python (Django, FastAPI, Celery), TypeScript, JavaScript, Node.js (Express), Bash — REST APIs, GraphQL, WebSockets, SDK development, connector design
- **Enterprise Integration:** Finacle core banking ↔ third-party systems integration, SMS and email gateway integrations, payment provider integrations with multi-provider failover, audit-grade structured logging via Filebeat to Elasticsearch
- **Cloud & Platforms:** AWS (EKS, ECS, Lambda, S3, SQS/SNS, EventBridge, DynamoDB, VPC), GCP (GKE, Cloud SQL), Azure, OCI, VMware, on-prem bare metal — Kubernetes (EKS, GKE, TKG, RKE2), Docker, Helm, Istio
- **Observability & Debugging:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry — cross-system root-cause analysis, telemetry-driven optimization, runbook authorship
- **CI/CD & IaC:** Terraform, Ansible, GitHub Actions, FluxCD, ArgoCD, Azure DevOps
- **Databases & Messaging:** PostgreSQL, MySQL, MongoDB, Redis, DynamoDB, Convex, Kafka, RabbitMQ, AWS SQS/SNS, EventBridge
- **Leadership:** Founded 4-person DevOps team and 12-person cross-functional team — customer-adjacent technical leadership, scoped project delivery, risk communication, stakeholder alignment

---

## Professional Certifications

- AI Engineering Specialization (ByteByteAI), Mar 2026
- Oracle Certified Architect Associate (Oracle), Aug 2025
- Oracle Certified DevOps Professional (Oracle), Aug 2025
- Oracle Certified Foundations Associate (Oracle), Jul 2025
- AWS Certified Cloud Practitioner (AWS), May 2024

---

## Professional Experience

### Core Banking Services Lead
**Guaranty Trust Bank Ghana LTD** | May 2025 - Present | Accra, Ghana

- Architected integrations between Finacle core banking and multiple third-party systems (transaction portals, internal tools), with audit-grade structured logging — enterprise-system integration inside the Bank of Ghana regulatory perimeter.
- Built bank-wide OTP service (Django + Next.js) integrating SMS and email gateways for 600+ internal users — customer-facing solution shipped end-to-end with structured Filebeat→Elasticsearch logging for audit.
- Built national ID verification service (Django + Next.js) processing and storing ID documents in self-hosted MinIO with automated verification workflows — independent end-to-end delivery against deadline.
- Use AI agents and prompt-engineered workflows to accelerate L2 incident triage and migration test design — coordinated 10,000+ test cases across 13 modules during the Basis-to-Finacle migration cutover.
- Run on-prem Finacle core banking on Tanzu Kubernetes Grid sustaining 1.5M+ daily transactions across 800+ production pods at 99.97% uptime.
- Lead L2 support operations correlating logs across internal apps and core banking microservices via Elastic Stack — cross-system debugging spanning network, data, application layers.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Founding CTO leading 12-person cross-functional team across product, design, mobile, frontend, backend, QA — daily stakeholder management with founders, investors, healthcare providers; customer-adjacent technical leadership as the platform's technical face.
- Architected the platform end-to-end across requirements gathering, system design, database modeling, API development; delivered three customer-facing applications (patient Flutter mobile, professional Flutter mobile, React admin web).
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS with multi-provider failover — production integration with external payment, SMS, and email gateways.
- Led performance optimizations reducing peak request latency by 90% via Redis caching, PostgreSQL query tuning and indexing — telemetry-driven optimization based on observed bottlenecks.
- Designed multi-cloud disaster recovery: AWS primary on EKS/ECS with Lambda; GCP secondary on GKE with Cloud SQL and Cloud Storage; mirrored IAM, dual CI/CD, regular failover drills.
- Automated application delivery and infrastructure provisioning via CI/CD pipelines on GitHub Actions and Terraform, making deployments repeatable, auditable, reversible.

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 - Present | Accra, Ghana

- Founded the bank's DevOps team of 4 engineers from zero — designed Git workflows, GitOps with FluxCD, declarative Helm config, security gates with Veracode + Trivy; delivered against rolling-release deadlines while building the practice in parallel.
- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests at 99.97% measured uptime including scheduled maintenance.
- Implemented CI/CD pipelines on GitHub Actions and Azure DevOps that cut deployment time by ~90% and increased release velocity ~5x; embedded Veracode + Trivy as automated security gates.
- Managed multi-cloud infrastructure across Azure and AWS: resource provisioning, private VPC peering to on-prem systems, IAM, access control.

---

## Projects

### career-ops — Multi-Mode AI Prompt Orchestration Framework
**Personal R&D** | 2025 - Present

- Build and maintain a working multi-mode prompt orchestration framework with explicit system-prompt + user-context separation, per-mode contracts, RAG retrieval over local knowledge bases, structured output schemas, prompt evaluation rubrics, version-controlled prompt library — used daily and applied to evaluate this UiPath FDE role itself.
- Implement LLM provider selection by capability/latency/cost tradeoffs — Claude as primary with prompt caching, OpenAI as fallback for specific tasks, retry-on-malformed-output logic, model-version pinning.
- Equivalent patterns to LangChain/LlamaIndex implemented as a custom orchestration layer for explicit control over routing, fallbacks, and structured output validation.
- **Stack:** Claude API, OpenAI API, Python, Node.js, RAG patterns, multi-agent orchestration, structured outputs, MCP-style tool-use

### AI Agents for Infrastructure Operations & Palsar Monitoring SaaS
**Personal R&D · Founder** | 2024 - Present

- Build specialized AI agents for QA automation, code review, and sysadmin operations against live Linux production servers — multi-agent orchestration, tool-use patterns, sandboxed execution, structured logging.
- Built Palsar (AI monitoring SaaS) on Claude API with prompt-engineered workflows producing structured outputs at scale — explicit output schemas, few-shot examples, model-version pinning, prompt caching for cost control.
- **Stack:** Claude API, Next.js, TypeScript, Convex, Python, AWS Lambda, EventBridge, DynamoDB, Linux production servers

### Virk Cloud (virk.cloud) — Production K8s PaaS
**Founder & CTO** | Aug 2025 - Present

- Architected and operate a self-service Platform-as-a-Service for startups with built-in CI/CD, observability, and log streaming on bare-metal VPS clusters with RKE2 Kubernetes — customer-facing developer experience focus.
- **Stack:** Next.js, TypeScript, Convex, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana, Python

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
