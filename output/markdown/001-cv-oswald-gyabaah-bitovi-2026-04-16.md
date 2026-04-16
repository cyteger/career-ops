<!-- career-ops:render format=letter language=en company="bitovi" date=2026-04-16 number=001 -->
# Oswald Gyabaah

**Full-Stack Software Engineer, AI-Enabled**

oswald.gyabaah@gmail.com | +233 55 413 4307 | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

Full-stack engineer with 6 years shipping production applications across web, mobile, backend, and infrastructure. Fluent in JavaScript/TypeScript, React, Next.js, Node.js, Python (Django, FastAPI), and Flutter, with deep CI/CD and cloud deployment experience. Founding CTO of MyHealthCop, where I led a 12-person cross-functional team and shipped a patient-facing mobile app, a health-professional app, and a React admin dashboard on AWS with GCP disaster recovery. Currently building AI agents for QA and infrastructure automation with Claude APIs, RAG, and multi-agent orchestration, and actively using AI-assisted development workflows for client and personal projects.

---

## Technical Skills

- **Frontend/Mobile:** JavaScript, TypeScript, React.js, Next.js, Tailwind CSS, Flutter, Web Components
- **Backend:** Python (Django, FastAPI, Celery), Node.js (Express), REST APIs, GraphQL, WebSockets
- **AI & Agents:** LLM API integration (Claude, OpenAI, Grok), RAG systems, AI agent development, multi-agent orchestration, tool-use patterns, AI-assisted development workflows
- **Databases:** PostgreSQL, MySQL, MongoDB, Firebase/Firestore, Convex, SQLite, Redis
- **Messaging & Queues:** AWS SQS/SNS, RabbitMQ, Redis queues, Kafka
- **Cloud & Infrastructure:** AWS (EKS, ECS, S3, SQS/SNS, VPC), GCP (GKE, Cloud SQL, Cloud Storage), Azure, OCI
- **Container Orchestration:** Docker, Docker Compose, Kubernetes (EKS, GKE, TKG, RKE2), Helm, Istio
- **CI/CD & GitOps:** Terraform, Ansible, GitHub Actions, ArgoCD, FluxCD, Azure DevOps, Codemagic, Jenkins
- **Observability:** Prometheus, Grafana, ELK Stack, Sentry
- **Project Management:** Agile/Scrum, Kanban, stakeholder management, full project lifecycle

---

## Professional Certifications

- AI Engineering Specialization (ByteByteAI), Mar 2026: Agents, RAG, LLM applications
- Oracle Certified DevOps Professional (Oracle), Aug 2025
- AWS Certified Cloud Practitioner (AWS), May 2024
- Database Structures and Management with MySQL (Coursera), Dec 2022
- Django Web Framework (Coursera), Dec 2022

---

## Professional Experience

### Guaranty Trust Bank Ghana LTD
**Apr 2024 - Present** | Accra, Ghana

**Team Lead, Core Banking Services** | May 2025 - Present

- Built a bank-wide OTP service using Next.js and Django, integrating SMS and email gateways, to secure core banking access for 600+ internal users with structured logging to Elasticsearch via Filebeat.
- Built a national ID verification service using Next.js and Django, processing and storing ID documents in self-hosted MinIO with automated verification and customer record updates.
- Architected integrations between Finacle core banking and third-party systems including transaction portals and internal tools.
- Led a 5-person QA team through the bank's Basis-to-Finacle migration cutover, designing and executing 10,000+ test cases across 13 core banking modules and 33 internal applications over a two-week window, covering integration, UAT, and peripheral device validation.
- Own the on-prem Finacle core banking deployment on Tanzu Kubernetes Grid, managing deployments, patching, and incident response across 800+ production pods to sustain 1.5M+ daily transactions.
- Extended the bank's observability stack into core banking with Finacle-specific dashboards for CPU/memory trends, transaction volumes, response times, and exceptions, plus threshold-based alerting.

**DevOps Engineering Lead** | Apr 2024 - Present

- Founded the bank's DevOps team of 4 engineers, replacing manual code handoffs with enforced Git workflows, containerized Kubernetes deployments, and automated release pipelines.
- Implemented CI/CD automation that cut deployment time by ~90% and increased release velocity ~5x; introduced GitOps with FluxCD for consistent repeatable deployments; integrated Veracode and Trivy scanning for automated security analysis.
- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests, with 99.97% measured uptime inclusive of monthly scheduled maintenance.
- Automated 95% of infrastructure configuration management using Ansible, Python, and Bash, turning multi-day manual processes into reproducible, version-controlled deployments.
- Introduced a unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting.
- Managed multi-cloud infrastructure across Azure and AWS: resource provisioning, private VPC links to on-prem systems, deployments, access control, and cost optimization.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Architected the myhealthcop.com platform end-to-end across requirements gathering, system design, database modeling, and API development, delivering three applications: a patient-facing Flutter mobile app (iOS + Android), a Flutter mobile app for health professionals, and a React admin web dashboard.
- Led a 12-person cross-functional team (frontend, backend, mobile, product, design, and QA) through full project lifecycle: requirements gathering, sprint planning, stakeholder management, and budgeting under Agile/Scrum.
- Designed secure, cost-efficient AWS infrastructure running containerized microservices on EKS and ECS with autoscaling, load balancing, and inter-service communication.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS, with SMS, email, and payment provider integrations including multi-provider failover.
- Automated application delivery and infrastructure provisioning via CI/CD pipelines on GitHub Actions and Terraform, making deployments repeatable, auditable, and reversible.
- Designed a disaster recovery strategy mirroring the AWS production environment on GCP using GKE, Cloud SQL, and Cloud Storage, with secure VPCs, IAM policies, and dual-environment CI/CD for rapid failover.

---

## Projects

### Digital-Recon: Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Building a real-time transaction reconciliation engine for financial institutions, detecting discrepancies across heterogeneous data sources including relational DBs, REST APIs, Elasticsearch, and Kafka topics, with configurable rules for automatic reconciliation or operator-reviewed flagging.
- Designed a Next.js/TypeScript triage dashboard enabling operators to define reconciliation rules, inspect flagged transactions, drill into source records across banking systems, and resolve mismatches with a full audit trail.
- Architected an event-driven processing layer using Kafka for upstream transaction ingestion and Celery for scheduled and on-demand reconciliation jobs, including windowed scans, per-source reprocessing, and downstream alerting.
- **Stack:** React, TypeScript, Python, Celery, Kafka, Elasticsearch, PostgreSQL, Docker

### Virk Cloud (virk.cloud)
**Founder & CTO** | Aug 2025 - Present

- Architected a Platform-as-a-Service for startups with built-in CI/CD, fixed billing, observability, real-time log streaming, and alerting.
- Built the full management console in Next.js with authentication, user management, real-time monitoring dashboards, and billing.
- Manage the underlying infrastructure on virtual private servers: RKE2 cluster deployment, hardware/storage provisioning, network and traffic management, and DNS.
- **Stack:** Next.js, JavaScript/TypeScript, Convex, Tailwind CSS, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana, Python
---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
