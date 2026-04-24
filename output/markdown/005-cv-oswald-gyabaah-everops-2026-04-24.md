<!-- career-ops:render format=letter language=en company="everops" date=2026-04-24 number=005 -->
# Oswald Gyabaah

**Senior DevOps Engineer — AWS EKS, Terraform, Platform Engineering**

oswald.gyabaah@gmail.com | +233 55 413 4307 | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

Senior DevOps Engineer with 6 years designing and running high-scale Kubernetes platforms in production. Founded Guaranty Trust Bank Ghana's DevOps team — CI/CD automation that cut deployment time ~90%, GitOps with FluxCD, and high-availability Kubernetes infrastructure on Azure and AWS with private VPC links to on-prem core banking. Manage 800+ production pods sustaining 1.5M+ daily banking transactions with 99.97% measured uptime. On AWS specifically: architected EKS + ECS microservices with Terraform IaC, IAM, VPC peering, SQS/SNS, and a disaster-recovery mirror on GCP. Currently operating a multi-tenant Kubernetes Platform-as-a-Service (Virk Cloud) with RKE2, FluxCD, and Terraform, and building AI agents for infrastructure automation.

---

## Core Competencies

- AWS EKS and multi-account architecture
- Terraform IaC for high-scale production
- GitOps: ArgoCD, FluxCD, GitHub Actions
- Kubernetes networking, RBAC, cluster security
- Multi-cloud (AWS, GCP, Azure, OCI) with VPC and IAM
- Observability with Prometheus, Grafana, ELK
- High-transaction fintech platform operations
- Platform engineering and internal developer platforms

---

## Technical Skills

- **Cloud & Infrastructure:** AWS (EKS, ECS, S3, SQS/SNS, VPC, IAM), Azure, GCP (GKE, Cloud SQL, Cloud Storage), OCI, VMware, on-prem bare metal (Tier III data centers)
- **Container Orchestration:** Docker, Docker Compose, Kubernetes (EKS, GKE, TKG/Tanzu, RKE2, AKS), Helm, Istio Service Mesh
- **IaC & GitOps:** Terraform, Ansible, FluxCD, ArgoCD, GitHub Actions, Azure DevOps, Jenkins, Codemagic
- **Observability:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry
- **Backend:** Python (FastAPI, Django, Celery), Node.js (Express), REST APIs, GraphQL, WebSockets
- **Databases:** PostgreSQL, MySQL, MongoDB, Redis, Firebase/Firestore, Convex, SQLite
- **Messaging & Queues:** AWS SQS/SNS, RabbitMQ, Redis queues, Kafka
- **AI & Agents:** LLM API integration (Claude, OpenAI), RAG systems, AI agent development, multi-agent orchestration, tool-use patterns

---

## Professional Certifications

- AWS Certified Cloud Practitioner (AWS), May 2024
- Oracle Certified DevOps Professional (Oracle), Aug 2025
- Oracle Certified Architect Associate (Oracle), Aug 2025
- Oracle Certified Foundations Associate (Oracle), Jul 2025
- AI Engineering Specialization (ByteByteAI), Mar 2026: Agents, RAG, LLM applications
- Database Structures and Management with MySQL (Coursera), Dec 2022
- Django Web Framework (Coursera), Dec 2022

---

## Professional Experience

### Guaranty Trust Bank Ghana LTD
**Apr 2024 - Present** | Accra, Ghana

**DevOps Engineering Lead** | Apr 2024 - Present

- Founded the bank's DevOps team of 4 engineers, replacing manual code handoffs with enforced Git workflows, containerized Kubernetes deployments, and automated release pipelines.
- Implemented CI/CD automation that cut deployment time by ~90% and increased release velocity ~5x; introduced GitOps with FluxCD for consistent, repeatable deployments across multiple clusters; integrated Veracode and Trivy scanning for automated security analysis.
- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests, with 99.97% measured uptime inclusive of monthly scheduled maintenance.
- Managed multi-cloud infrastructure across AWS and Azure: resource provisioning, private VPC peering to on-prem systems, IAM, access control, and cost optimization.
- Automated 95% of infrastructure configuration management using Terraform, Ansible, Python, and Bash, turning multi-day manual processes into reproducible, version-controlled deployments.
- Implemented declarative, version-controlled cluster deployments with FluxCD, Helm, and Azure DevOps for consistency, idempotency, and rapid disaster recovery rebuilds.
- Introduced a unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting, reducing mean time to resolution on production incidents.

**Team Lead, Core Banking Services** | May 2025 - Present

- Own the on-prem Finacle core banking deployment on Tanzu Kubernetes Grid, managing deployments, patching, and incident response across 800+ production pods to sustain 1.5M+ daily transactions.
- Extended the bank's observability stack into core banking with Finacle-specific dashboards for CPU/memory trends, transaction volumes, response times, and exceptions, plus threshold-based alerting for proactive scaling.
- Led L2 incident response, correlating logs across internal apps and core banking microservices via the Elastic Stack for root-cause analysis and remediation.
- Led a 5-person QA team through the bank's Basis-to-Finacle migration cutover, designing and executing 10,000+ test cases across 13 core banking modules and 33 internal applications over a two-week window.
- Architected integrations between Finacle core banking and third-party systems including transaction portals and internal tools.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Designed secure, cost-efficient AWS infrastructure running containerized microservices on EKS and ECS with autoscaling, load balancing, and inter-service communication.
- Automated application delivery and infrastructure provisioning via CI/CD pipelines on GitHub Actions and Terraform, making deployments repeatable, auditable, and reversible.
- Designed a disaster recovery strategy mirroring the AWS production environment on GCP using GKE, Cloud SQL, and Cloud Storage, with secure VPCs, IAM policies, and dual-environment CI/CD for rapid failover.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS, with multi-provider failover.
- Led performance optimizations that reduced peak request latency by 90% through Redis caching, query tuning, and indexing in PostgreSQL.
- Led a 12-person cross-functional team through full project lifecycle under Agile/Scrum: requirements, sprint planning, stakeholder management, and budgeting.

---

## Projects

### Virk Cloud (virk.cloud)
**Founder & CTO** | Aug 2025 - Present

- Architected a multi-tenant Platform-as-a-Service for startups with built-in CI/CD, fixed billing, observability, real-time log streaming, and alerting — an internal developer platform pattern at commercial scale.
- Built the full management console in Next.js with authentication, user management, real-time monitoring dashboards, and billing.
- Manage the underlying infrastructure on virtual private servers: RKE2 cluster deployment, hardware/storage provisioning, network and traffic management, and DNS.
- **Stack:** Kubernetes (RKE2), Terraform, FluxCD, Prometheus, Grafana, Next.js, Convex, Python

### Digital-Recon: Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Building a real-time transaction reconciliation engine for financial institutions, detecting discrepancies across heterogeneous data sources including relational DBs, REST APIs, Elasticsearch, and Kafka topics.
- Architected an event-driven processing layer using Kafka for upstream transaction ingestion and Celery for scheduled and on-demand reconciliation jobs, including windowed scans, per-source reprocessing, and downstream alerting.
- **Stack:** Kafka, Celery, Python, Elasticsearch, PostgreSQL, Docker, Next.js, TypeScript

### AI Agents for Infrastructure Operations
**Personal R&D** | 2024 - Present

- Building specialized AI agents for QA automation, code review, and sysadmin operations, running against live Linux production servers with real workloads.
- Prototyping agent-driven SaaS tools using RAG, tool-use, and multi-agent orchestration patterns.
- Completed AI Engineering Specialization (ByteByteAI) covering agents, RAG, and LLM application development.

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
