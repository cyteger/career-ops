<!-- career-ops:render format=letter language=en company="glearn" date=2026-04-16 number=003 -->
# Oswald Gyabaah

**AI Software Engineer — Full-Stack & AI Agent Orchestration**

oswald.gyabaah@gmail.com | +233 55 413 4307 | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

Full-stack engineer with 6 years shipping production applications across web, mobile, backend, and infrastructure. Founding CTO of MyHealthCop, where I took the platform from zero to launch on AWS with GCP disaster recovery, led a 12-person cross-functional team, and shipped three applications including two Flutter iOS + Android apps and a React admin dashboard. Daily-driver stack is Next.js, React, TypeScript, and Python, with hands-on AI-agent orchestration: I'm currently running specialized Claude-based agents for QA, code review, and sysadmin against live Linux production servers, using RAG, tool-use, and multi-agent patterns. Ashesi graduate based in Accra with native context on the Ghanaian/WAEC education landscape.

---

## Technical Skills

- **Frontend/Mobile:** JavaScript, TypeScript, React.js, Next.js, Tailwind CSS, Flutter (iOS + Android), Web Components
- **Backend:** Python (FastAPI, Django, Celery), Node.js (Express), REST APIs, GraphQL, WebSockets
- **AI & Agents:** LLM API integration (Claude, OpenAI, Grok), RAG systems, AI agent development, multi-agent orchestration, tool-use patterns, structured output parsing, AI-assisted development workflows (Claude Code)
- **Databases & Managed Platforms:** PostgreSQL, Convex, Supabase-equivalent real-time DBs, MySQL, MongoDB, Firebase/Firestore, Redis
- **Deployment & Platforms:** Vercel-class hosting, Kubernetes (EKS, GKE, RKE2), Docker, serverless patterns
- **Messaging & Queues:** AWS SQS/SNS, Kafka, Redis queues, RabbitMQ
- **Testing:** Jest, React Testing Library, Cypress, Playwright E2E, pytest, UAT coordination
- **Cloud:** AWS (EKS, ECS, S3, SQS/SNS, VPC), GCP (GKE, Cloud SQL, Cloud Storage), Azure, OCI
- **CI/CD:** GitHub Actions, Azure DevOps, Codemagic, Terraform, Ansible, FluxCD, ArgoCD
- **Observability:** Prometheus, Grafana, ELK Stack, Sentry
- **Project Management:** Agile/Scrum, stakeholder management, full project lifecycle

---

## Professional Certifications

- AI Engineering Specialization (ByteByteAI), Mar 2026: Agents, RAG, LLM applications
- Oracle Certified DevOps Professional (Oracle), Aug 2025
- Oracle Certified Architect Associate (Oracle), Aug 2025
- Oracle Certified Foundations Associate (Oracle), Jul 2025
- AWS Certified Cloud Practitioner (AWS), May 2024

---

## Professional Experience

### Guaranty Trust Bank Ghana LTD
**Apr 2024 - Present** | Accra, Ghana

**Team Lead, Core Banking Services** | May 2025 - Present

- Built a bank-wide OTP service using Next.js and Django, integrating SMS and email gateways, to secure core banking access for 600+ internal users with structured logging to Elasticsearch via Filebeat.
- Built a national ID verification service using Next.js and Django, processing and storing ID documents in self-hosted MinIO with automated verification and customer record updates.
- Architected integrations between Finacle core banking and third-party systems including transaction portals and internal tools.
- Led a 5-person QA team through the bank's Basis-to-Finacle migration cutover, designing and executing 10,000+ test cases across 13 core banking modules and 33 internal applications over a two-week window.
- Own the on-prem Finacle core banking deployment on Tanzu Kubernetes Grid, managing deployments, patching, and incident response across 800+ production pods to sustain 1.5M+ daily transactions.

**DevOps Engineering Lead** | Apr 2024 - Present

- Founded the bank's DevOps team of 4 engineers, replacing manual code handoffs with enforced Git workflows, containerized Kubernetes deployments, and automated release pipelines.
- Implemented CI/CD automation that cut deployment time by ~90% and increased release velocity ~5x; introduced GitOps with FluxCD.
- Architected high-availability Kubernetes clusters handling 3M+ daily requests, with 99.97% measured uptime.
- Introduced a unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Took the platform from 0 to 1 as founding CTO: requirements gathering, system design, database modeling, API development, team hiring, and delivery across three applications — a patient-facing Flutter mobile app (iOS + Android), a Flutter mobile app for health professionals (iOS + Android), and a React admin web dashboard.
- Led a 12-person cross-functional team (frontend, backend, mobile, product, design, and QA) through full project lifecycle: requirements, sprint planning, stakeholder management, and budgeting under Agile/Scrum.
- Designed secure, cost-efficient AWS infrastructure running containerized microservices on EKS and ECS with autoscaling, load balancing, and inter-service communication.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS, with SMS, email, and payment provider integrations including multi-provider failover.
- Led performance optimizations that reduced peak request latency by 90% through Redis caching, query tuning, and indexing in PostgreSQL.
- Designed a disaster recovery strategy mirroring the AWS production environment on GCP using GKE, Cloud SQL, and Cloud Storage, with secure VPCs, IAM policies, and dual-environment CI/CD for rapid failover.
- Automated application delivery and infrastructure provisioning via CI/CD pipelines on GitHub Actions and Terraform.

---

## Projects

### AI Agents for Infrastructure Operations
**Personal R&D** | 2024 - Present

- Building specialized AI agents for QA automation, code review, and sysadmin operations, running against live Linux production servers with real workloads.
- Orchestrating multi-agent workflows using Claude Code, RAG over runbooks, tool-use patterns, structured output parsing, and HITL approval gates.
- Actively using AI-assisted development workflows (Claude Code + agents) to parallelize feature work across my own projects while preserving code-review rigor.
- Completed AI Engineering Specialization (ByteByteAI) covering agents, RAG, and LLM application development.

### Virk Cloud (virk.cloud)
**Founder & CTO** | Aug 2025 - Present

- Architected a multi-tenant Platform-as-a-Service for startups with built-in CI/CD, fixed billing, observability, real-time log streaming, and alerting — a Vercel-class platform built from scratch.
- Built the full management console in Next.js with authentication, user management, real-time monitoring dashboards, and billing; backed by Convex for real-time state (same category as Supabase).
- Manage the underlying infrastructure on virtual private servers: RKE2 cluster deployment, hardware/storage provisioning, network and traffic management, and DNS.
- **Stack:** Next.js, TypeScript, Convex, Tailwind CSS, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana, Python

### Digital-Recon: Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Building a real-time transaction reconciliation engine for financial institutions, detecting discrepancies across heterogeneous data sources including relational DBs, REST APIs, Elasticsearch, and Kafka topics.
- Designed a Next.js/TypeScript triage dashboard enabling operators to define reconciliation rules, inspect flagged transactions, drill into source records, and resolve mismatches with a full audit trail.
- Architected an event-driven processing layer using Kafka for ingestion and Celery for scheduled and on-demand reconciliation jobs.
- **Stack:** Next.js, TypeScript, Python, Celery, Kafka, Elasticsearch, PostgreSQL, Docker

### Vistara: Property Tenant Assessment Platform
**Founder** | 2026 - Present

- Multi-app platform helping renters evaluate housing conditions before signing leases.
- Built landing page, tenant web app, admin web dashboard, and admin Flutter mobile app (iOS in TestFlight, Android in beta) for field data collection.
- **Stack:** Next.js, React, TypeScript, Flutter, Codemagic CI/CD

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
