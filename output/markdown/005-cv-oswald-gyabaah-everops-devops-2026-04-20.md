<!-- career-ops:render format=letter language=en company="everops-devops" date=2026-04-20 number=005 -->
# Oswald Gyabaah

**Senior DevOps / Platform Engineer — EKS, Multi-Cloud, GitOps at Enterprise Scale**

oswald.gyabaah@gmail.com | +233 55 413 4307 | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

Senior DevOps / Platform Engineer with 6 years building and running enterprise Kubernetes at scale. Founded GTBank Ghana's DevOps practice from zero — 4-engineer team, 800+ production pods, 99.97% uptime across 3M+ daily requests, and a GitOps pipeline that cut deployment time ~90%. Architected cloud-native platforms on AWS EKS and GCP GKE, with Terraform IaC, ArgoCD / FluxCD, AWS Secrets Manager + KMS, and Prometheus + Grafana observability. Currently building AI agents for infrastructure automation and an internal developer platform (Virk Cloud) on RKE2. Fintech background with 1.5M+ daily banking transactions.

---

## Technical Skills

- **Cloud & Kubernetes:** AWS (EKS, ECS, VPC, IAM, KMS, Secrets Manager, SQS/SNS), GCP (GKE, Cloud SQL, Cloud Storage), Azure, OCI, on-prem (TKG/Tanzu, RKE2), Helm, Istio service mesh
- **Infrastructure as Code:** Terraform (multi-env, modules), Ansible, Python + Bash automation, declarative deployments
- **GitOps & CI/CD:** ArgoCD, FluxCD, GitHub Actions, Azure DevOps, Jenkins, Veracode + Trivy security scanning
- **Observability:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry
- **Security & Identity:** AWS IAM (roles, policies, boundaries), KMS, Secrets Manager, OAuth2/OIDC, Keycloak, JWT
- **Platform & Backend:** Python (Django, FastAPI, Celery), Node.js, REST/GraphQL/WebSockets, PostgreSQL, Redis, Kafka, RabbitMQ
- **AI & Agents:** Claude API, multi-agent orchestration, tool-use, RAG, AI agents for sysadmin and QA on production Linux

---

## Professional Certifications

- Oracle Certified DevOps Professional (Oracle), Aug 2025
- Oracle Certified Architect Associate (Oracle), Aug 2025
- AWS Certified Cloud Practitioner (AWS), May 2024
- AI Engineering Specialization (ByteByteAI), Mar 2026: Agents, RAG, LLM applications

---

## Professional Experience

### Guaranty Trust Bank Ghana LTD
**Apr 2024 - Present** | Accra, Ghana

**DevOps Engineering Lead** | Apr 2024 - Present

- Founded the bank's DevOps team of 4 engineers from zero — introduced enforced Git workflows, containerized Kubernetes deployments, and automated release pipelines replacing manual code handoffs.
- Architected HA Kubernetes clusters running internal applications at 3M+ daily requests with 99.97% measured uptime, auto-scaling, and self-healing, with declarative cluster configs via FluxCD + Helm + Azure DevOps.
- Implemented CI/CD automation that cut deployment time by ~90% and increased release velocity ~5x; integrated Veracode and Trivy scanning for automated security analysis on every merge.
- Automated 95% of infrastructure configuration using Terraform, Ansible, Python, and Bash — turning multi-day manual processes into reproducible, version-controlled minutes.
- Managed multi-cloud infrastructure across Azure and AWS: VPC networking, private links to on-prem systems, IAM-based access control, and cost optimization across environments.
- Introduced a unified observability stack (Prometheus, Grafana, ELK, Sentry) for centralized logging, tracing, and alerting, cutting incident MTTR across production services.

**Team Lead, Core Banking Services** | May 2025 - Present

- Own the on-prem Finacle deployment on Tanzu Kubernetes Grid (TKG), operating 800+ production pods with Istio service mesh, RBAC-based multi-tenant isolation, and Helm-managed releases sustaining 1.5M+ daily banking transactions.
- Extended Prometheus/Grafana observability into core banking with Finacle-specific dashboards (CPU/memory trends, transaction volumes, response times, exceptions) plus threshold-based alerting for proactive scaling.
- Led a 5-person QA team through the bank's Basis-to-Finacle migration cutover, executing 10,000+ test cases across 13 core banking modules and 33 internal applications in a two-week window.
- Architected integrations between Finacle core banking and third-party systems, with structured logging to Elasticsearch via Filebeat for audit and incident response.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Architected the platform end-to-end on AWS EKS and ECS with autoscaling, VPC peering, and inter-service communication, designed for multi-environment account isolation from day one.
- Provisioned infrastructure with Terraform and automated application delivery through GitHub Actions CI/CD, making deployments repeatable, auditable, and reversible across Dev/Staging/Prod.
- Designed a multi-cloud disaster recovery strategy mirroring AWS EKS onto GCP GKE, with secure VPCs, IAM policies, KMS-managed secrets, and dual-environment CI/CD for rapid failover.
- Built a high-throughput background processing system on AWS SQS/SNS handling 1M+ daily jobs (payments, messaging, notifications) with multi-provider failover.
- Cut peak request latency by 90% through Redis caching, query tuning, and PostgreSQL indexing, with observability gates before each release.
- Led a 12-person cross-functional team (frontend, backend, mobile, product, design, QA) through full project lifecycle under Agile/Scrum.

---

## Projects

### Virk Cloud (virk.cloud) — Internal Developer Platform
**Founder & CTO** | Aug 2025 - Present

- Built an internal developer platform on RKE2 Kubernetes with FluxCD GitOps, Terraform-provisioned infrastructure, per-tenant namespace isolation, and self-service deployments — the same platform-engineering patterns used at hyperscalers.
- Designed the management console in Next.js with authentication, billing, real-time monitoring, and log streaming; hardened multi-tenant isolation at networking, IAM, and container layers.
- **Stack:** Kubernetes (RKE2), Docker, FluxCD, Terraform, Next.js, Convex, Prometheus, Grafana, Python, Bash

### AI Agents for Infrastructure Operations
**Personal R&D** | 2024 - Present

- Building specialized AI agents for QA automation, code review, and sysadmin operations — running against live Linux production servers with RAG over runbooks, tool-use, and human-in-the-loop approval gates.
- Prototyping agent-driven SaaS tools using Claude Code, multi-agent orchestration, and production-safe execution patterns.

### Digital-Recon — Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Event-driven reconciliation engine for financial institutions, ingesting from Kafka topics, REST APIs, and Elasticsearch, with Celery-scheduled scans and configurable rules for auto or operator-reviewed flagging.
- **Stack:** React, TypeScript, Python, Celery, Kafka, Elasticsearch, PostgreSQL, Docker

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
