# Oswald Gyabaah

**Full-Stack Software and Infrastructure Engineer**

oswald.gyabaah@gmail.com | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

Platform engineer and solutions architect with 6 years building and operating production systems at scale across on-prem and cloud environments. Founded GTBank Ghana's DevOps practice from scratch and runs the core banking platform behind 1.5M+ daily financial transactions. Founding CTO of MyHealthCop, leading a 12-person team and architecting mobile, web, and backend systems end to end. Currently building AI agents for infrastructure operations.

---

## Technical Skills

- **Frontend/Mobile:** JavaScript, TypeScript, React.js, Next.js, Tailwind CSS, Flutter
- **Backend:** Python (Django, FastAPI, Celery), Node.js (Express), REST APIs, GraphQL, WebSockets
- **Databases:** PostgreSQL, MySQL, MongoDB, Firebase/Firestore, DynamoDB (single-table and multi-table designs), Convex, SQLite, Redis
- **Messaging & Queues:** AWS SQS/SNS, AWS EventBridge, RabbitMQ, Redis queues, Kafka
- **Testing:** Jest, React Testing Library, Cypress, Playwright E2E, pytest, UAT coordination
- **Cloud & Infrastructure:** AWS (EKS, ECS, Lambda, S3, SQS/SNS, EventBridge, DynamoDB, VPC), GCP (GKE, Cloud SQL, Cloud Storage), Azure, OCI, VMware, on-prem bare metal (Tier III data centers)
- **Container Orchestration:** Docker, Docker Compose, Kubernetes (EKS, GKE, TKG/Tanzu, RKE2), Helm, Istio Service Mesh
- **CI/CD & GitOps:** Terraform, Ansible, GitHub Actions, ArgoCD, FluxCD, Azure DevOps, Codemagic, Jenkins
- **Observability:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry
- **AI & Agents:** LLM API integration (Claude, OpenAI, Grok), RAG systems, AI agent development, multi-agent orchestration, tool-use patterns, AI-assisted development workflows
- **Project Management:** Full project lifecycle (requirements through delivery), Agile/Scrum, Kanban, stakeholder management, risk assessment

---

## Professional Certifications

- AI Engineering Specialization (ByteByteAI), Mar 2026
- Oracle Certified DevOps Professional (Oracle), Aug 2025
- Oracle Certified Architect Associate (Oracle), Aug 2025
- Oracle Certified Foundations Associate (Oracle), Jul 2025
- AWS Certified Cloud Practitioner (AWS), May 2024
- Django Web Framework (Coursera), Dec 2022

---

## Professional Experience

### Core Banking Services Lead
**Guaranty Trust Bank Ghana LTD** | May 2025 - Present | Accra, Ghana

- Own the on-prem Finacle core banking deployment on Tanzu Kubernetes Grid (TKG), managing deployments, patching, and incident response across 800+ production pods to sustain 1.5M+ daily transactions.
- Own application-tier disaster recovery for the core banking estate, partnering with the database and network teams to recover all 268 applications to a standby DR data center at a 45-minute RTO and near-zero RPO. Authored the DR policy and recovery runbooks, and lead bank-wide failover simulations involving 600+ staff.
- Built parallel deployment pipelines in Jenkins with selectable primary and DR targets, keeping the two sites in continuous parity, and automated container image mirroring across their self-hosted Harbor registries to keep the environments fully independent.
- Lead L2 support operations, correlating logs across internal apps and core banking microservices via the Elastic Stack for root-cause analysis and remediation.
- Led a 5-person QA team through the bank's Basis-to-Finacle migration cutover, designing and executing 10,000+ test cases across 13 core banking modules and 33 internal applications over a two-week window, covering integration, UAT, and peripheral device validation.
- Extended the bank's observability stack into core banking with Finacle-specific dashboards for CPU/memory trends, transaction volumes, response times, and exceptions, plus threshold-based alerting for proactive scaling.
- Architected integrations between Finacle core banking and third-party systems including transaction portals and internal tools.
- Built a bank-wide OTP service using Next.js and Django, integrating SMS and email gateways, to secure core banking access for 600+ internal users with structured logging to Elasticsearch via Filebeat.
- Built a national ID verification service using Next.js and Django, processing and storing ID documents in self-hosted MinIO with automated verification and customer record updates.

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 - Present | Accra, Ghana

- Founded the bank's DevOps team of 4 engineers, replacing manual code handoffs with enforced Git workflows, containerized Kubernetes deployments, and automated release pipelines
- Implemented CI/CD automation that cut deployment time by ~90% and increased release velocity ~5x; introduced GitOps with FluxCD for consistent repeatable deployments; integrated Veracode and Trivy scanning for automated security analysis
- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests, with 99.97% measured uptime inclusive of monthly scheduled maintenance; implemented auto-scaling and self-healing mechanisms
- Automated 95% of infrastructure configuration management using Ansible, Python, and Bash scripts, turning multi-day manual processes into reproducible, version-controlled deployments in minutes
- Implemented declarative, version-controlled cluster deployments with FluxCD, Helm, and Azure DevOps for consistency, idempotency, and rapid disaster recovery rebuilds
- Introduced a unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting, reducing mean time to resolution on production incidents
- Managed multi-cloud infrastructure across Azure and AWS: resource provisioning, private VPC links to on-prem systems, deployments, access control and cost optimization

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Architected the myhealthcop.com platform end-to-end across requirements gathering, system design, database modeling, and API development, delivering three applications: a patient-facing Flutter mobile app (iOS + Android), a Flutter mobile app for health professionals, and a React admin web dashboard.
- Designed secure, cost-efficient AWS infrastructure running containerized microservices on EKS and ECS alongside Lambda functions for event-driven workloads, with autoscaling, load balancing, and inter-service communication.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS, with SMS, email, and payment provider integrations including multi-provider failover.
- Led performance optimizations that reduced peak request latency by 90% through Redis caching, query tuning, and indexing in PostgreSQL.
- Automated application delivery and infrastructure provisioning via CI/CD pipelines on GitHub Actions and Terraform, making deployments repeatable, auditable, and reversible.
- Designed a disaster recovery strategy mirroring the AWS production environment on GCP using GKE, Cloud SQL, and Cloud Storage, with secure VPCs, IAM policies, and dual-environment CI/CD for rapid failover.
- Led a 12-person cross-functional team (frontend, backend, mobile, product, design, and QA) through full project lifecycle: requirements gathering, sprint planning, stakeholder management, and budgeting under Agile/Scrum

---

## Projects

### Digital-Recon: Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Building a real-time transaction reconciliation engine for financial institutions to detect discrepancies across heterogeneous data sources including relational DBs, APIs, Elasticsearch, etc in realtime.
- Architected an event-driven processing layer using Kafka for upstream transaction ingestion and Celery for scheduled and on-demand reconciliation jobs.
- **Stack:** React, TypeScript, Python, Celery, Kafka, Elasticsearch, PostgreSQL, Docker

### Virk Cloud (virk.cloud)
**Founder & CTO** | Aug 2025 - Present

- Architected a Platform-as-a-Service for startups with built-in CI/CD, observability and log streaming
- Built a management console for workload management, custom domains and monitoring dashboards
- Manage underlying infra on private VPS including cluster deployment, hardware and network provisioning
- **Stack:** Next.js, JavaScript/TypeScript, Convex, Tailwind CSS, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana, Python

### Vistara: Property Tenant Assessment Platform
**Founder** | 2026 - Present

- Multi-app platform helping renters evaluate housing conditions (water, electricity, safety, noise) before signing leases
- Built landing page, tenant web app (assessment form), admin web dashboard, and admin mobile app (Flutter) for field data collection
- iOS mobile app in TestFlight; web apps deployed to beta
- **Stack:** Next.js, React, TypeScript, Flutter, Codemagic CI/CD

### AI Agents for Infrastructure Operations
**Personal R&D** | 2024 - Present

- Building specialized AI agents for QA automation, code review, and sysadmin operations, running against live Linux production servers with real workloads
- Prototyping agent-driven SaaS tools using RAG, tool-use, and multi-agent orchestration patterns
- Built AWS Lambda functions triggered by EventBridge to deliver notifications on codebase events
- Used DynamoDB for NoSQL data modeling across personal projects, with both single-table and multi-table design patterns
- Completed AI Engineering Specialization (ByteByteAI) covering agents, RAG, and LLM application development

### Education Research and Innovation Foundry (erifoundry.org)
**Founder & Research Lead** | Oct 2025 - Present

- Leading design of AI-driven research initiatives in adaptive learning, cognitive modeling, and educational analytics
- Coordinating cross-disciplinary research on ML and software tooling for education
- Prototyping applications of LLMs in human-centered learning systems

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana

