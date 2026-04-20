<!-- career-ops:render format=letter language=en company="everops" date=2026-04-20 number=004 -->
# Oswald Gyabaah

**Senior Software Engineer — Identity, QA & Testing Infrastructure**

oswald.gyabaah@gmail.com | +233 55 413 4307 | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

Senior engineer with 6 years shipping production systems across testing, security, backend, and Kubernetes infrastructure. Led a 5-person QA team at GTBank Ghana through a core banking migration with 10,000+ unit, integration, and UAT test cases across 13 modules. Built bank-wide OTP, national ID verification, and Keycloak/OIDC integrations for 600+ users; run 800+ production pods on Kubernetes at 1.5M+ daily transactions. Advanced Bash and Python automation on Linux/macOS, Docker everywhere, AWS IAM in production, messaging with SQS/SNS, Kafka, and RabbitMQ. Currently building Claude-based AI agents for QA and code review on live Linux servers.

---

## Technical Skills

- **Testing:** Jest, React Testing Library, Cypress, Playwright E2E, pytest, UAT coordination, integration testing across microservices
- **Identity & Security:** OAuth2, OIDC, Keycloak, LDAP, JWT, AWS IAM, VPC design, bank-grade access control
- **Containers & Orchestration:** Docker, Docker Compose, Kubernetes (EKS, GKE, TKG/Tanzu, RKE2), Helm, Istio
- **Automation & Scripting:** Advanced Bash on Linux/macOS, Python (FastAPI, Django, Celery), Ansible, Terraform
- **Backend & Messaging:** Node.js (Express), REST/GraphQL/WebSockets, Kafka, RabbitMQ, AWS SQS/SNS, Redis queues
- **Cloud & CI/CD:** AWS, GCP, Azure, OCI; GitHub Actions, Azure DevOps, FluxCD, ArgoCD, Veracode & Trivy scanning
- **Observability & Data:** Prometheus, Grafana, ELK Stack, Sentry; PostgreSQL, MySQL, MongoDB, Redis, Elasticsearch
- **AI & Agents:** Claude API, RAG, multi-agent orchestration, tool-use, AI-assisted code review workflows

---

## Professional Certifications

- AI Engineering Specialization (ByteByteAI), Mar 2026: Agents, RAG, LLM applications
- Oracle Certified DevOps Professional & Architect Associate (Oracle), Aug 2025
- AWS Certified Cloud Practitioner (AWS), May 2024

---

## Professional Experience

### Guaranty Trust Bank Ghana LTD
**Apr 2024 - Present** | Accra, Ghana

**Team Lead, Core Banking Services** | May 2025 - Present

- Led a 5-person QA team through the bank's Basis-to-Finacle migration, designing and executing 10,000+ unit, integration, and UAT test cases across 13 core banking modules and 33 internal applications under a two-week cutover window.
- Built a bank-wide OTP and access control service (Next.js + Django) for 600+ internal users, plus a national ID verification service handling document ingestion and customer record updates on self-hosted MinIO.
- Performed code reviews across internal engineering teams, enforcing standards for security, performance, and readability on Python, Node.js, and Next.js services.
- Own the on-prem Finacle deployment on Tanzu Kubernetes Grid (TKG), managing deployments, patching, and incident response across 800+ production pods sustaining 1.5M+ daily transactions with Docker and Helm.

**DevOps Engineering Lead** | Apr 2024 - Present

- Founded the bank's DevOps team of 4 engineers, standardizing Git workflows, code review gates, containerized Kubernetes deployments, and automated release pipelines.
- Automated 95% of infrastructure configuration using Ansible, Python, and advanced Bash scripting; integrated Veracode + Trivy scanning for security analysis on every merge.
- Architected HA Kubernetes clusters handling 3M+ daily requests at 99.97% uptime, with a unified observability stack (Prometheus, Grafana, ELK, Sentry).

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Architected the platform end-to-end as founding CTO: system design, AWS IAM and VPC policies, database modeling, and API development across patient, practitioner, and admin apps.
- Built a high-throughput event-driven processing system handling 1M+ daily jobs with SQS/SNS and multi-provider failover, on containerized microservices on EKS and ECS.
- Cut peak request latency by 90% through Redis caching, query tuning, and PostgreSQL indexing, with regression tests and monitoring gates.
- Designed a disaster-recovery strategy mirroring AWS onto GCP with secure VPCs, IAM policies, and dual-environment CI/CD.
- Led a 12-person cross-functional team through the full project lifecycle under Agile/Scrum, with code review and test gates on every pull request.

---

## Projects

### AI Agents for QA & Code Review
**Personal R&D** | 2024 - Present

- Building specialized AI agents for QA automation and code review, running against live Linux production servers and real codebases — flagging regressions, security issues, and style violations before human review.
- Orchestrating multi-agent workflows using Claude Code, RAG over runbooks and style guides, tool-use patterns, and human-in-the-loop approval gates for production changes.
- Completed AI Engineering Specialization (ByteByteAI) covering agents, RAG, and LLM application development.

### Virk Cloud (virk.cloud)
**Founder & CTO** | Aug 2025 - Present

- Architected a multi-tenant PaaS on bare-metal VPS with RKE2 Kubernetes, Docker, FluxCD, and Terraform, including container-based test environments for customer workloads.
- Hardened multi-tenant isolation at networking, IAM, and container layers; automated cluster bootstrap and tenant provisioning with advanced Bash and Python.
- **Stack:** Kubernetes (RKE2), Docker, FluxCD, Terraform, Next.js, Convex, Python, Bash

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
