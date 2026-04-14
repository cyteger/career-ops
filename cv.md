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
- Built a national ID verification service using Next.js and Python, to process and store ID documents in self-hosted MinIO bucket with automated verification and customer record updates.

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 - Present | Accra, Ghana

- Founded the bank's DevOps team of 4 engineers and established modern delivery practices, introducing Kubernetes, containerized deployments, disciplined version control, and automated release workflows
- Implemented CI/CD automation that cut deployment time by ~90% and increased release velocity ~5x; introduced GitOps with FluxCD for consistent repeatable deployments; integrated Veracode and Trivy scanning for automated security analysis
- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests with 99.97% uptime SLA; implemented auto-scaling and self-healing mechanisms
- Automated 95% of infrastructure configuration management using Ansible, Python, and Bash scripts, turning multi-day manual processes into reproducible, version-controlled deployments in minutes
- Implemented stateless, version-controlled cluster deployments with FluxCD, Helm, and Azure DevOps for consistency, idempotency, and rapid disaster recovery cluster rebuilds
- Introduced unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting to accelerate RCA and improve mean time to resolution
- Managed multi-cloud infrastructure across Azure and AWS: resource provisioning, private VPC links to on-prem systems, deployments, access control and cost optimization

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024

- Architected the myhealthcop.com platform end-to-end across requirements gathering, system design, database modeling, and API development, delivering three applications: a patient-facing mobile app, a health professional mobile app, and an admin web dashboard.
- Designed secure, cost-efficient AWS infrastructure running containerized microservices on EKS and ECS with autoscaling, load balancing, and inter-service communication.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS, with SMS, email, and payment provider integrations including failover and provider fallback.
- Led performance optimizations that reduced peak request latency by 90% through Redis caching, query tuning, and indexing in PostgreSQL.
- Automated application delivery and infrastructure provisioning via CI/CD pipelines on GitHub Actions and Terraform, making deployments repeatable, auditable, and reversible while reducing manual error.
- Designed a disaster recovery strategy mirroring the AWS production environment on GCP using GKE, Cloud SQL, and Cloud Storage, with secure VPCs, IAM policies, and dual-environment CI/CD for rapid failover.
- Led a 12-person cross-functional team (frontend, backend, mobile, product, design, and QA) through full project lifecycle: requirements gathering, sprint planning, stakeholder management, risk assessment, and budgeting under Agile/Scrum

---

## Projects

### Digital-Recon: Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Built a real-time transaction reconciliation engine for financial institutions, detecting discrepancies across heterogeneous data sources including relational DBs, REST APIs, Elasticsearch, and Kafka topics, with configurable rules for automatic reconciliation or operator-reviewed flagging.
- Designed a Next.js/TypeScript triage dashboard enabling operators to define reconciliation rules, inspect flagged transactions, drill into source records across banking systems, and resolve mismatches with a full audit trail.
- Architected an event-driven processing layer using Kafka for upstream transaction ingestion and Celery for scheduled and on-demand reconciliation jobs, including windowed scans, per-source reprocessing, and downstream alerting.
- **Stack:** React, TypeScript, Python, Celery, Kafka, Elasticsearch, PostgreSQL, Docker

### Virk Cloud (virk.cloud)
**Founder & CTO** | Aug 2025

- Architected a production-grade Platform-as-a-service with inbuilt CI/CD that enables startups to deploy instantly with fixed billing, built-in observability, real-time log streaming, and alerts
- Built the full management console in Next.js with authentication, user management, real-time monitoring dashboards, and billing
- Manage full infrastructure on virtual private servers: cluster deployment (RKE2), hardware/storage provisioning, network/traffic management, DNS maintenance
- **Stack:** Next.js, JavaScript/TypeScript, Convex, Tailwind CSS, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana, python

### Vistara: Property Tenant Assessment Platform
**Founder** | 2026 - Present

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

