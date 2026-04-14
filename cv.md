# Oswald Gyabaah

**Full-Stack Software and Infrastructure Engineer**

oswald.gyabaah@gmail.com | +233 55 413 4307 | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

Full-stack engineer with 6 years building, shipping, and scaling production systems end-to-end across React/Next.js frontends, Python/Node backends, and Kubernetes infrastructure. Led a 12-person cross-functional team as founding CTO (MyHealthCop), founded GTBank Ghana's DevOps practice from scratch, and now builds AI agents for infrastructure automation and QA. Equally strong in Python and JavaScript/TypeScript. Ships across web (React, Next.js), mobile (Flutter, iOS + Android), backend (Django, FastAPI, Node.js), and infrastructure (Kubernetes, Terraform, multi-cloud). Currently building AI-powered SaaS products using RAG, tool-use, and multi-agent orchestration patterns.

---

## Technical Skills

- **Frontend/Mobile:** JavaScript, TypeScript, React.js, Next.js, Tailwind CSS, Flutter
- **Backend:** Python (Django, FastAPI, Celery), Node.js (Express), REST APIs, GraphQL, WebSockets
- **Databases:** PostgreSQL, MySQL, MongoDB, Firebase/Firestore, Convex, SQLite, Redis
- **Messaging & Queues:** AWS SQS/SNS, RabbitMQ, Redis queues, Kafka
- **Testing:** Jest, React Testing Library, Cypress, Playwright E2E, pytest, UAT coordination
- **Cloud & Infrastructure:** AWS (EKS, ECS, S3, SQS/SNS, VPC), GCP (GKE, Cloud SQL, Cloud Storage), Azure, OCI, VMware, on-prem bare metal (Tier III data centers)
- **Container Orchestration:** Docker, Docker Compose, Kubernetes (EKS, GKE, TKG/Tanzu, RKE2), Helm, Istio Service Mesh
- **CI/CD & GitOps:** Terraform, Ansible, GitHub Actions, ArgoCD, FluxCD, Azure DevOps, Codemagic, Jenkins
- **Observability:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry
- **AI & Agents:** LLM API integration (Claude, OpenAI, Grok), RAG systems, AI agent development, multi-agent orchestration, tool-use patterns, AI-assisted development workflows
- **Project Management:** Full project lifecycle (requirements through delivery), Agile/Scrum, Kanban, stakeholder management, risk assessment
---

## Professional Certifications

- AI Engineering Specialization (ByteByteAI), Mar 2026: Agents, RAG, LLM applications
- Oracle Kubernetes Engine Specialist (Oracle), Aug 2025
- Certified Oracle Cloud Infrastructure DevOps Professional (Oracle), Aug 2025
- Oracle Certified Cloud Infrastructure Architect Associate (Oracle), Aug 2025
- Oracle Certified Foundations Associate (Oracle), Jul 2025
- AWS Certified Cloud Practitioner (AWS), May 2024
- Database Structures and Management with MySQL (Coursera), Dec 2022
- Django Web Framework (Coursera), Dec 2022

---

## Professional Experience

### Team Lead, Core Banking Services
**Guaranty Trust Bank Ghana LTD** | May 2025 - Present
- Own the on-prem Finacle core banking deployment on Tanzu Kubernetes Grid (TKG), managing deployments, patching, and incident response across 800+ production pods to sustain 1.5M+ daily transactions.
- Lead L2 support operations, leveraging the Elastic Stack to correlate logs across internal apps and core banking microservices for root-cause analysis and remediation.
- Led end-to-end QA for the bank's Basis-to-Finacle migration, designing and executing 10,000+ test cases across 13 core banking modules and 33 internal applications, covering integration, UAT, and peripheral device validation.
- Built the observability stack, delivering dashboards tracking CPU/memory trends, transaction volumes, response times, and exceptions, with threshold-based alerting to drive proactive scaling.
- Architected integrations between Finacle core banking and third-party systems including transaction portals, internal tools, and auxiliary services.
- Built a bank-wide OTP service using Next.js and Django, integrating SMS and email gateways, to secure core banking access for 600+ internal users with structured logging to Elasticsearch via Filebeat.
- Built an identity verification service using Next.js, Python/Celery, and Redis, with self-hosted MinIO document storage and automated customer record updates.

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 - May 2025 | Accra, Ghana

- Founded the bank's DevOps team of 4 engineers and led junior engineers to establish modern delivery practices, introducing Kubernetes, containerized deployments, disciplined version control, and automated release workflows
- Implemented CI/CD automation that cut deployment time by ~90% and increased release velocity ~5x; introduced GitOps with FluxCD for consistent repeatable deployments; integrated Veracode and Trivy scanning for automated security analysis
- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests with 99.97% uptime SLA; implemented auto-scaling and self-healing mechanisms
- Automated 95% of infrastructure configuration management using Ansible, Python, and Bash scripts, turning multi-day manual processes into reproducible, version-controlled deployments in minutes
- Implemented stateless, version-controlled cluster deployments with FluxCD, Helm, and Azure DevOps for consistency, idempotency, and rapid disaster recovery cluster rebuilds
- Introduced unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting to accelerate RCA and improve mean time to resolution
- Managed multi-cloud infrastructure across Azure and AWS: resource provisioning, private VPC links to on-prem systems, deployments, access control, cost optimization, and reliable operation of GTExpress and GTWorld

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024

- Founded the technical organization and recruited/managed a 12-person cross-functional team: 2 frontend (React), 3 backend (including self), 2 mobile (Flutter), 2 product managers, 2 designers, 1 QA engineer
- Architected the full myhealthcop.com platform end-to-end, covering requirements gathering, system design, database modeling, and API architecture. Delivered three distinct applications: a patient-facing web portal (React), a Flutter mobile app (iOS + Android, published to App Store and Play Store), and an admin management dashboard (React)
- Designed secure, cost-efficient AWS infrastructure orchestrating containerized microservices using EKS and ECS with autoscaling, load balancing, and seamless inter-service communication
- Built a high-throughput background processing system handling 1M+ daily jobs (payments, messaging, notifications) using SQS/SNS with SMS, email, and payment provider integrations including failover and provider fallback
- Reduced peak latency by 90% through database query tuning, caching layers (Redis), and indexing across PostgreSQL
- Automated infrastructure provisioning with Terraform, reducing setup time by 90% while building CI/CD pipelines to streamline deployments and minimize human errors
- Designed and implemented disaster recovery: parallel GCP production environment mirroring AWS using GKE, Cloud SQL, and Cloud Storage with secure VPCs, IAM policies, and dual-environment CI/CD for rapid failover
- Managed full project lifecycle: requirements gathering, sprint planning, stakeholder management, risk assessment, budgeting, and delivery across Agile/Scrum methodology

---

## Projects

### Digital-Recon: Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Built a real-time transaction reconciliation engine for financial institutions that detects discrepancies across multiple data sources (PostgreSQL, REST APIs, Elasticsearch, Kafka topics) and flags mismatches for operator review
- **Frontend:** React + TypeScript triage dashboard where operators view flagged transactions, drill into source records across banking systems, and resolve mismatches with a full audit trail
- **Backend:** Python service layer exposing ingestion, reconciliation-rule, and resolution APIs with role-based access control
- **Real-time processing:** Celery workers run scheduled and on-demand reconciliation jobs, including windowed scans, per-source reprocessing, and alert generation
- **Event streaming:** Kafka consumers ingest transaction events from upstream banking systems; producers emit reconciliation outcomes to downstream topics for alerting and analytics
- **Data layer:** PostgreSQL stores reconciliation state and resolution history; Elasticsearch indexes high-volume transaction records and logs for fast lookups and aggregations
- Fully containerized with Docker for reproducible local development and deployments
- **Stack:** React, TypeScript, Python, Celery, Kafka, Elasticsearch, PostgreSQL, Docker

### Virk Cloud (virk.cloud)
**Founder & CTO** | Aug 2025

- Architected a production-grade Kubernetes PaaS (comparable to Vercel) that enables startups to deploy clusters instantly without operational overhead, with fixed billing, built-in observability, real-time log streaming, and alerts
- Built the full management console in Next.js with authentication, cluster management, real-time monitoring dashboards, billing, and state management, deployed on the platform itself
- Manage full infrastructure on virtual private servers: cluster deployment (RKE2), hardware/storage provisioning, network/traffic management, DNS maintenance
- Automated all deployments using FluxCD and Terraform for reproducible, version-controlled operations
- **Stack:** Next.js, TypeScript, Tailwind CSS, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana

### Vistara: Property Tenant Assessment Platform
**Founder** | 2025 - Present

- Multi-app platform helping renters evaluate housing conditions (water, electricity, safety, noise) before signing leases
- Built landing page, tenant web app (assessment form), admin web dashboard, and admin mobile app (Flutter) for field data collection
- Currently in TestFlight (iOS) with web version hosted
- **Stack:** Next.js, React, TypeScript, Flutter, Codemagic CI/CD

### AI Agents for Infrastructure Operations
**Personal R&D** | 2024 - Present

- Building specialized AI agents for QA automation, code review, and sysadmin operations on production Linux servers, fully operational against real systems
- Developing agent-driven SaaS products leveraging RAG, tool-use, and multi-agent orchestration patterns
- Completed AI Engineering Specialization (ByteByteAI) covering agents, RAG, and LLM application development

### Education Research and Innovation Foundry (erifoundry.org)
**Founder & Research Lead** | Oct 2025 - Present

- Leading design of AI-driven research initiatives in adaptive learning, cognitive modeling, and educational analytics
- Coordinating cross-disciplinary research to develop experimental frameworks for scalable ML and software solutions in education
- Prototyping applications of LLMs in human-centered learning systems

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana

---

## Writing & Community

- **risingEngineers** (Substack): technical blog on software engineering and infrastructure
- **GTBank DevOps**: trained and mentored 3 junior engineers in Kubernetes, CI/CD, and GitOps practices
- **MyHealthCop**: built and led a 12-person cross-functional engineering organization from zero
