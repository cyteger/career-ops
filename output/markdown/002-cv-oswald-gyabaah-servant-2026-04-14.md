<!-- career-ops:render format=letter language=en company="Servant" date=2026-04-14 number=002 -->
# Oswald Gyabaah

**DevOps & Cloud Engineer — Azure & Backend Enablement**

oswald.gyabaah@gmail.com | +233 55 413 4307 | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana (UTC+0)

---

## Professional Summary

DevOps and cloud engineer with 6 years building and operating production infrastructure on Azure, AWS, and GCP. Founded GTBank Ghana's DevOps practice from scratch — multi-cloud Azure + AWS footprint with private VPC links to on-prem, Terraform + FluxCD GitOps, CI/CD that cut deployment time ~90%, and 800+ pods sustaining 1.5M+ daily transactions at 99.97% uptime. Backend-aware: ships Python (FastAPI, Django, Celery) services as part of platform work, not as a separate skill. Built Virk Cloud, an independent multi-tenant Kubernetes PaaS, end-to-end. Comfortable owning reliability, scalability, and delivery velocity for revenue-ready, secure, enterprise-grade systems.

---

## Core Competencies

- Azure Cloud Engineering (App Services, AKS, Functions, Key Vault — adjacent via AWS analogues)
- Multi-Cloud Infrastructure (Azure, AWS, GCP, OCI)
- Infrastructure-as-Code (Terraform, Ansible)
- CI/CD and GitOps (Azure DevOps, GitHub Actions, FluxCD, ArgoCD)
- Kubernetes Operations at Scale (AKS-adjacent: TKG, EKS, GKE, RKE2)
- Backend Enablement (Python, FastAPI, Django, Celery)
- Cloud Security and Networking (VPC, IAM, secrets management)
- Observability and Incident Response (Prometheus, Grafana, ELK, Sentry)

---

## Technical Skills

- **Cloud & Infrastructure:** Azure, AWS (EKS, ECS, S3, SQS/SNS, VPC), GCP (GKE, Cloud SQL, Cloud Storage), OCI, on-prem bare metal (Tier III data centers)
- **CI/CD & GitOps:** Terraform, Ansible, Azure DevOps, GitHub Actions, FluxCD, ArgoCD, Helm, Codemagic
- **Container Orchestration:** Docker, Docker Compose, Kubernetes (AKS-adjacent: TKG/Tanzu, EKS, GKE, RKE2), Istio Service Mesh
- **Observability:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Azure Monitor (adjacent), Sentry
- **Security & Networking:** Private VPC peering, IAM, Key Vault / AWS SSM / Secrets Manager, Veracode, Trivy, secure CI/CD gates
- **Backend:** Python (FastAPI, Django, Celery), Node.js (Express), REST APIs, GraphQL, WebSockets
- **Databases & Messaging:** PostgreSQL, MySQL, MongoDB, Redis, Kafka, AWS SQS/SNS, RabbitMQ
- **Frontend (when needed):** TypeScript, React, Next.js, Tailwind CSS
- **AI & Agents:** Claude / OpenAI API integration, RAG systems, AI agent development for ops automation, tool-use patterns

---

## Professional Certifications

- AI Engineering Specialization (ByteByteGo), Mar 2026: Agents, RAG, LLM applications
- Oracle Kubernetes Engine Specialist (Oracle), Aug 2025
- Certified Oracle Cloud Infrastructure DevOps Professional (Oracle), Aug 2025
- Oracle Certified Cloud Infrastructure Architect Associate (Oracle), Aug 2025
- AWS Certified Cloud Practitioner (AWS), May 2024
- Django Web Framework (Coursera), Dec 2022

---

## Professional Experience

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 - Present

- Managed multi-cloud infrastructure across Azure and AWS: resource provisioning, private VPC links to on-prem systems, deployments, access control, and cost optimization.
- Implemented CI/CD automation across Azure DevOps and GitHub Actions that cut deployment time by ~90% and increased release velocity ~5x; introduced GitOps with FluxCD for repeatable, idempotent deployments; integrated Veracode and Trivy security scanning into pipelines.
- Founded the bank's DevOps team of 4 engineers and established modern delivery practices, introducing Kubernetes, containerized deployments, disciplined version control, and automated release workflows.
- Architected high-availability Kubernetes clusters running internal applications handling 3M+ daily requests with 99.97% uptime; implemented auto-scaling and self-healing.
- Automated 95% of infrastructure configuration management using Terraform, Ansible, Python, and Bash, turning multi-day manual processes into reproducible, version-controlled deployments in minutes.
- Stood up unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting to accelerate RCA.

### Team Lead, Core Banking Services
**Guaranty Trust Bank Ghana LTD** | May 2025 - Present

- Own the on-prem Finacle deployment on Tanzu Kubernetes Grid (AKS-equivalent managed K8s), managing 800+ production pods sustaining 1.5M+ daily transactions.
- Built a bank-wide OTP service (Next.js + Django + Celery + Redis), integrating SMS and email gateways, securing core banking access for 600+ internal users with structured logging to Elasticsearch via Filebeat.
- Built an identity verification service using Python/FastAPI-equivalent (Django + Celery), Redis, and self-hosted MinIO document storage with automated customer record updates.
- Lead L2 support operations, leveraging Elastic Stack to correlate logs across internal apps and core banking microservices for root-cause analysis.
- Architected integrations between Finacle core banking and third-party systems including transaction portals and internal tools.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024

- Designed secure, cost-efficient AWS infrastructure running containerized microservices on EKS and ECS with autoscaling, load balancing, and secure inter-service communication via VPCs and IAM policies.
- Automated application delivery and infrastructure provisioning via CI/CD on GitHub Actions and Terraform, making deployments repeatable, auditable, and reversible.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS with multi-provider failover.
- Designed a disaster recovery strategy mirroring the AWS production environment on GCP using GKE, Cloud SQL, and Cloud Storage, with secure VPCs, IAM policies, and dual-environment CI/CD for rapid failover.
- Led performance optimizations that reduced peak request latency by 90% through Redis caching, query tuning, and PostgreSQL indexing.
- Led a 12-person cross-functional team (frontend, backend, mobile, product, design, QA) under Agile/Scrum, directly client-facing across product cycles.

---

## Projects

### Virk Cloud (virk.cloud)
**Founder & CTO** | Aug 2025

- Architected and operate a production-grade multi-tenant Kubernetes PaaS (Vercel-style) with built-in CI/CD, observability, real-time log streaming, and fixed billing.
- Manage full infrastructure on virtual private servers: RKE2 cluster deployment, FluxCD-driven tenant onboarding, hardware and storage provisioning, network/traffic management, DNS.
- Built the management console in Next.js with authentication, cluster management, real-time monitoring dashboards, and billing — deployed onto the platform itself.
- **Stack:** Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana, Next.js, TypeScript, Convex

### Digital-Recon: Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Built a real-time event-driven transaction reconciliation engine for financial institutions, detecting discrepancies across heterogeneous data sources (relational DBs, REST APIs, Elasticsearch, Kafka topics).
- Architected an event-driven processing layer using Kafka for upstream ingestion and Celery for scheduled and on-demand reconciliation jobs, with windowed scans, per-source reprocessing, and downstream alerting.
- Deployed on Docker with PostgreSQL and Elasticsearch backends; designed for serverless-style horizontal scale-out per workload.
- **Stack:** Python, Celery, Kafka, Elasticsearch, PostgreSQL, Docker, Next.js, TypeScript

### AI Agents for Infrastructure Operations
**Personal R&D** | 2024 - Present

- Building production-shaped AI agents for QA automation, code review, and sysadmin operations against real Linux and Kubernetes systems, using Claude API with tool-use, dry-run mode, and human escalation gates.
- Applying agent-driven patterns (RAG, tool-use, multi-agent orchestration) to support AI/ML workloads in production-adjacent contexts.
- Completed AI Engineering Specialization (ByteByteGo) covering agents, RAG, and LLM application development.

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
