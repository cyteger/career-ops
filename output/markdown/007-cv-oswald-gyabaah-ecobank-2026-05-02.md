<!-- career-ops:render format=a4 language=en company="ecobank" date=2026-05-02 number=007 -->
# Oswald Gyabaah

**Senior Infrastructure & Architecture Engineer — Cloud, Kubernetes, Banking**

oswald.gyabaah@gmail.com | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

Infrastructure and architecture engineer with 6 years designing and operating enterprise systems at bank scale, all inside the Bank of Ghana regulatory perimeter. Founded Guaranty Trust Bank Ghana's DevOps practice from zero and currently own the on-prem Finacle core banking deployment on Tanzu Kubernetes Grid sustaining 1.5M+ daily transactions. Lead technical project management and architecture design for cross-functional bank initiatives, integrating Finacle with multiple third-party systems. Architected a multi-cloud healthtech platform on AWS with GCP disaster recovery as founding CTO of MyHealthCop, leading architecture decisions across compute, networking, security, and data layers. Multi-cloud experience spans AWS, GCP, Azure, OCI, VMware, and on-prem bare metal.

---

## Core Competencies

- Enterprise architecture and platform design
- Multi-cloud architecture (AWS, GCP, Azure, OCI)
- Kubernetes architecture at enterprise scale
- Security-aware infrastructure (IAM, OAuth2, IaC scanning, VPC)
- API-driven systems and microservices integration
- Architecture governance and operational resilience
- Technical project management and cross-functional leadership
- Bank of Ghana regulatory perimeter and audit-ready delivery

---

## Technical Skills

- **Cloud & Architecture:** AWS (EKS, ECS, Lambda, S3, SQS/SNS, EventBridge, DynamoDB, VPC, IAM), GCP (GKE, Cloud SQL, Cloud Storage), Azure, OCI, VMware vSphere, on-prem bare metal (Tier III data centers)
- **Container Orchestration & Platforms:** Docker, Docker Compose, Kubernetes (EKS, GKE, TKG/Tanzu, RKE2), Helm, Istio Service Mesh, FluxCD, ArgoCD
- **Security & Identity:** IAM, OAuth2, OIDC, Keycloak, JWT, WAF, Veracode, Trivy, structured audit logging via Filebeat
- **Integration & APIs:** REST APIs, GraphQL, WebSockets, Kafka, RabbitMQ, AWS SQS/SNS, AWS EventBridge, Redis queues
- **IaC & CI/CD:** Terraform, Ansible, GitHub Actions, Azure DevOps, Codemagic, Jenkins
- **Observability:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry
- **Databases:** PostgreSQL, MySQL, MongoDB, Firebase/Firestore, DynamoDB (single-table and multi-table), Convex, SQLite, Redis
- **Languages:** Python (Django, FastAPI, Celery), Node.js (Express), JavaScript, TypeScript, Bash
- **Frontend:** React.js, Next.js, Tailwind CSS, Flutter
- **AI & Emerging Tech:** LLM API integration (Claude, OpenAI), RAG systems, AI agents, multi-agent orchestration

---

## Professional Certifications

- Oracle Certified Architect Associate (Oracle), Aug 2025
- Oracle Certified DevOps Professional (Oracle), Aug 2025
- Oracle Certified Foundations Associate (Oracle), Jul 2025
- AWS Certified Cloud Practitioner (AWS), May 2024
- AI Engineering Specialization (ByteByteAI), Mar 2026
- Django Web Framework (Coursera), Dec 2022

---

## Professional Experience

### Core Banking Services Lead
**Guaranty Trust Bank Ghana LTD** | May 2025 - Present | Accra, Ghana

- Architected integrations between Finacle core banking and multiple third-party systems including transaction portals and internal tools, operating inside the Bank of Ghana regulatory perimeter.
- Lead technical project management for cross-functional bank initiatives, translating business requirements into architecture decisions and coordinating delivery across business and technology teams.
- Own the on-prem Finacle core banking deployment on Tanzu Kubernetes Grid, managing deployments, patching, and incident response across 800+ production pods to sustain 1.5M+ daily transactions.
- Built a bank-wide OTP service (Django + Next.js) integrating SMS and email gateways to secure core banking access for 600+ internal users, with structured logging to Elasticsearch via Filebeat for audit.
- Built a national ID verification service (Django + Next.js) processing and storing ID documents in self-hosted MinIO with automated verification workflows.
- Lead L2 support operations correlating logs across internal apps and core banking microservices via the Elastic Stack for root-cause analysis and remediation.
- Led a 5-person QA team through the Basis-to-Finacle migration cutover, designing and executing 10,000+ test cases across 13 core banking modules and 33 internal applications over a two-week window.
- Extended the bank's observability stack into core banking with Finacle-specific dashboards and threshold-based alerting for proactive scaling.

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 - Present | Accra, Ghana

- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests at 99.97% measured uptime.
- Founded the bank's DevOps team of 4 engineers, replacing manual code handoffs with enforced Git workflows, containerized Kubernetes deployments, and automated release pipelines.
- Embedded Veracode and Trivy scanning into release pipelines as automated security gates; introduced GitOps with FluxCD for declarative, version-controlled cluster deployments and rapid disaster recovery rebuilds.
- Implemented CI/CD automation that cut deployment time by ~90% and increased release velocity ~5x.
- Managed multi-cloud infrastructure across Azure and AWS: resource provisioning, private VPC peering to on-prem systems, IAM, access control, and cost optimization.
- Automated 95% of infrastructure configuration management using Terraform, Ansible, Python, and Bash, turning multi-day manual processes into reproducible, version-controlled deployments.
- Introduced a unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Architected the myhealthcop.com platform end-to-end across requirements gathering, system design, database modeling, and API development, delivering three applications: a patient-facing Flutter mobile app, a Flutter app for health professionals, and a React admin web dashboard.
- Led architecture decisions across compute, networking, security, and data layers; defined API contracts, data models, and inter-service communication patterns for the three client applications and the backend microservices.
- Designed cost-efficient AWS infrastructure running containerized microservices on EKS and ECS alongside Lambda functions for event-driven workloads, with autoscaling, load balancing, and IAM-controlled inter-service communication.
- Designed a disaster recovery strategy mirroring the AWS production environment on GCP using GKE, Cloud SQL, and Cloud Storage, with secure VPCs, IAM policies, and dual-environment CI/CD for rapid failover.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS with multi-provider failover.
- Led performance optimizations that reduced peak request latency by 90% through Redis caching, query tuning, and indexing in PostgreSQL.
- Led a 12-person cross-functional team (frontend, backend, mobile, product, design, QA) through the full Agile lifecycle from requirements to delivery, including sprint planning, stakeholder management, and budgeting.

---

## Projects

### Virk Cloud (virk.cloud) — Platform-as-a-Service
**Founder & CTO** | Aug 2025 - Present

- Architected a Platform-as-a-Service for startups with built-in CI/CD, observability, and log streaming on bare-metal VPS clusters.
- Built a management console for workload management, custom domains, and monitoring dashboards.
- Manage underlying infrastructure including cluster deployment, hardware and network provisioning.
- **Stack:** Next.js, TypeScript, Convex, Tailwind CSS, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana, Python

### Digital-Recon — Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Building a real-time reconciliation engine for financial institutions to detect discrepancies across heterogeneous data sources (relational DBs, APIs, Elasticsearch) in real time.
- Architected an event-driven processing layer using Kafka for upstream transaction ingestion and Celery for scheduled and on-demand reconciliation jobs.
- **Stack:** React, TypeScript, Python, Celery, Kafka, Elasticsearch, PostgreSQL, Docker

### AI Agents for Infrastructure Operations
**Personal R&D** | 2024 - Present

- Building specialized AI agents for QA automation, code review, and sysadmin operations, running against live Linux production servers with real workloads.
- Prototyping agent-driven SaaS tools using RAG, tool-use, and multi-agent orchestration patterns.
- Built AWS Lambda functions triggered by EventBridge to deliver notifications on codebase events.

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
