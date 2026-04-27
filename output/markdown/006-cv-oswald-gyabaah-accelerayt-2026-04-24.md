<!-- career-ops:render format=letter language=en company="accelerayt" date=2026-04-24 number=006 -->
# Oswald Gyabaah

**Senior Full-Stack Engineer — React, Next.js, Node.js, AWS**

oswald.gyabaah@gmail.com | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

Former CTO and Senior Full-Stack Engineer with 6 years shipping production JavaScript/TypeScript across React/Next.js, Node.js, and AWS serverless (Lambda, EventBridge, DynamoDB). Founded and shipped MyHealthCop's web, mobile, and admin platforms; led the GTBank Basis-to-Finacle migration cutover across 33 applications in two weeks.

---

- Full-stack JavaScript and TypeScript
- React and Next.js production applications
- Node.js (Express) and Python (FastAPI, Django) backends
- AWS Lambda, EventBridge, and DynamoDB
- NoSQL data modelling: DynamoDB (single-table and multi-table), MongoDB, Firestore
- AWS infrastructure and Terraform IaC (CloudFormation-adjacent)
- Inheriting and evolving live production codebases
- Mission-driven product delivery

---

## Technical Skills

- **Frontend:** JavaScript, TypeScript, React.js, Next.js, Tailwind CSS
- **Mobile:** Flutter (iOS + Android), Codemagic CI/CD
- **Backend:** Node.js (Express), Python (FastAPI, Django, Celery), REST APIs, GraphQL, WebSockets
- **Databases (NoSQL):** DynamoDB (single-table and multi-table designs), MongoDB, Firebase/Firestore, Convex, Redis
- **Databases (SQL):** PostgreSQL, MySQL, SQLite
- **AWS:** Lambda, EventBridge, DynamoDB, EKS, ECS, S3, SQS/SNS, VPC, IAM
- **Other cloud:** Azure, GCP (GKE, Cloud SQL, Cloud Storage), OCI
- **IaC & CI/CD:** Terraform, Ansible, GitHub Actions, FluxCD, ArgoCD, Azure DevOps, Codemagic, Jenkins
- **Containers & Orchestration:** Docker, Docker Compose, Kubernetes (EKS, GKE, TKG, RKE2), Helm
- **Messaging & Queues:** AWS SQS/SNS, Kafka, RabbitMQ, Redis queues
- **Observability:** Prometheus, Grafana, ELK Stack, Sentry
- **AI & Agents:** LLM API integration (Claude, OpenAI), RAG systems, agent development, tool-use patterns

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

- Built a bank-wide OTP service using Django (Python) and Next.js (React/TypeScript), integrating SMS and email gateways, to secure core banking access for 600+ internal users with structured logging to Elasticsearch via Filebeat.
- Built a national ID verification service using Django and Next.js, processing and storing ID documents in self-hosted MinIO with automated verification and customer record updates.
- Led a 5-person QA team through the bank's Basis-to-Finacle core banking migration cutover, designing and executing 10,000+ test cases across 13 core banking modules and 33 internal applications over a two-week window, covering integration, UAT, and peripheral device validation.
- Own the on-prem Finacle core banking deployment on Tanzu Kubernetes Grid, managing deployments, patching, and incident response across 800+ production pods to sustain 1.5M+ daily transactions.
- Led L2 incident response, correlating logs across internal apps and core banking microservices via the Elastic Stack for root-cause analysis and remediation.

**DevOps Engineering Lead** | Apr 2024 - Present

- Founded the bank's DevOps team of 4 engineers, replacing manual code handoffs with enforced Git workflows, containerized Kubernetes deployments, and automated release pipelines.
- Implemented CI/CD automation that cut deployment time by ~90% and increased release velocity ~5x; introduced GitOps with FluxCD for consistent, repeatable deployments; integrated Veracode and Trivy scanning for automated security analysis.
- Architected high-availability Kubernetes clusters across multiple environments running internal applications handling 3M+ daily requests, with 99.97% measured uptime inclusive of monthly scheduled maintenance.
- Managed multi-cloud infrastructure across AWS and Azure: resource provisioning, private VPC peering to on-prem systems, IAM, access control, and cost optimization.
- Automated 95% of infrastructure configuration management using Terraform, Ansible, Python, and Bash, turning multi-day manual processes into reproducible, version-controlled deployments.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Architected the myhealthcop.com platform end-to-end across requirements, system design, database modeling, and API development, delivering three applications: a patient-facing Flutter mobile app (iOS + Android), a Flutter app for health professionals, and a React admin web dashboard.
- Designed secure, cost-efficient AWS infrastructure running containerized microservices on EKS and ECS alongside Lambda functions for event-driven workloads, with autoscaling, load balancing, and inter-service communication.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS, with SMS, email, and payment provider integrations including multi-provider failover.
- Led performance optimizations that reduced peak request latency by 90% through Redis caching, query tuning, and indexing in PostgreSQL.
- Automated application delivery and infrastructure provisioning via CI/CD pipelines on GitHub Actions and Terraform, making deployments repeatable, auditable, and reversible.
- Led a 12-person cross-functional team (frontend, backend, mobile, product, design, QA) through full project lifecycle under Agile/Scrum.

---

## Projects

### Virk Cloud (virk.cloud)
**Founder & CTO** | Aug 2025 - Present

- Architected a multi-tenant Platform-as-a-Service for startups with built-in CI/CD, fixed billing, observability, real-time log streaming, and alerting.
- Built the full management console in Next.js (React, TypeScript) with authentication, user management, real-time monitoring dashboards, and billing — inherited-and-evolved an early prototype into production.
- Manage the underlying infrastructure on virtual private servers: RKE2 cluster deployment, hardware/storage provisioning, network and traffic management, and DNS.
- **Stack:** Next.js, React, TypeScript, Convex, Tailwind CSS, Kubernetes (RKE2), Terraform, FluxCD, Prometheus, Grafana, Python

### Digital-Recon: Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Building a real-time transaction reconciliation engine for financial institutions, detecting discrepancies across heterogeneous data sources including relational DBs, REST APIs, Elasticsearch, and Kafka topics.
- Designed a Next.js/TypeScript triage dashboard enabling operators to define reconciliation rules and resolve mismatches with a full audit trail.
- Architected an event-driven processing layer using Kafka for upstream ingestion and Celery for scheduled and on-demand reconciliation jobs.
- **Stack:** React, TypeScript, Next.js, Python, Celery, Kafka, Elasticsearch, PostgreSQL, Docker

### Education Research and Innovation Foundry (erifoundry.org)
**Founder & Research Lead** | Oct 2025 - Present

- Leading design of AI-driven research initiatives in adaptive learning, cognitive modeling, and educational analytics.
- Coordinating cross-disciplinary research on ML and software tooling for education.
- Prototyping applications of LLMs in human-centered learning systems.

### AI Agents for Infrastructure Operations
**Personal R&D** | 2024 - Present

- Building specialized AI agents for QA automation, code review, and sysadmin operations, running against live Linux production servers with real workloads.
- Built AWS Lambda functions triggered by EventBridge to deliver notifications on codebase events.
- Used DynamoDB for NoSQL data modeling across personal projects, with both single-table and multi-table design patterns.

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
