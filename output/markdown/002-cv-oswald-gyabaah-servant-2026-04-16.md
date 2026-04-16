<!-- career-ops:render format=letter language=en company="servant" date=2026-04-16 number=002 -->
# Oswald Gyabaah

**DevOps & Cloud Engineer — Azure, Kubernetes, Python**

oswald.gyabaah@gmail.com | +233 55 413 4307 | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

Senior DevOps and Cloud Engineer with 6 years building and running production platforms across multi-cloud environments. Founded GTBank Ghana's DevOps team — CI/CD automation that cut deployment time ~90%, GitOps with FluxCD, and high-availability Kubernetes infrastructure on Azure and AWS with private VPC links to on-prem core banking. Deep Kubernetes experience managing 800+ production pods on Tanzu Kubernetes Grid sustaining 1.5M+ daily banking transactions. Shipped production FastAPI, Django, and Node.js services with structured observability via Prometheus, Grafana, and the Elastic Stack. Currently building AI agents for QA and infrastructure automation that run against live Linux production servers, and operating a multi-tenant Kubernetes PaaS (Virk Cloud) built with Terraform and RKE2.

---

## Core Competencies

- Azure DevOps & Multi-Cloud Infrastructure
- Terraform & Infrastructure-as-Code
- Kubernetes (AKS, TKG, RKE2, EKS, GKE)
- CI/CD Pipelines (Azure DevOps, GitHub Actions)
- FastAPI & Python Backend Enablement
- Multi-Tenant SaaS Platform Engineering
- Cloud Security & Networking
- Observability & Incident Response

---

## Technical Skills

- **Cloud & Infrastructure:** Azure, AWS (EKS, ECS, S3, SQS/SNS, VPC), GCP (GKE, Cloud SQL, Cloud Storage), OCI, VMware, on-prem bare metal
- **Container Orchestration:** Docker, Docker Compose, Kubernetes (AKS, EKS, GKE, TKG, RKE2), Helm, Istio Service Mesh
- **CI/CD & GitOps:** Azure DevOps, GitHub Actions, Terraform, Ansible, ArgoCD, FluxCD, Codemagic, Jenkins
- **Backend:** Python (FastAPI, Django, Celery), Node.js (Express), REST APIs, GraphQL, WebSockets
- **Observability:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry
- **Security & Networking:** VPC/Subnets, Private Peering, IAM, WAF, OAuth2/Keycloak, OIDC, LDAP, JWT
- **Databases:** PostgreSQL, MySQL, MongoDB, Redis, Firebase/Firestore, Convex, SQLite
- **Messaging & Queues:** AWS SQS/SNS, RabbitMQ, Redis queues, Kafka
- **Testing:** Jest, React Testing Library, Cypress, Playwright E2E, pytest, UAT coordination
- **AI & Agents:** LLM API integration (Claude, OpenAI, Grok), RAG systems, AI agent development, multi-agent orchestration, tool-use patterns
- **Frontend/Mobile:** JavaScript, TypeScript, React.js, Next.js, Tailwind CSS, Flutter

---

## Professional Certifications

- AI Engineering Specialization (ByteByteAI), Mar 2026: Agents, RAG, LLM applications
- Oracle Certified DevOps Professional (Oracle), Aug 2025
- Oracle Certified Architect Associate (Oracle), Aug 2025
- Oracle Certified Foundations Associate (Oracle), Jul 2025
- AWS Certified Cloud Practitioner (AWS), May 2024
- Database Structures and Management with MySQL (Coursera), Dec 2022
- Django Web Framework (Coursera), Dec 2022

---

## Professional Experience

### Guaranty Trust Bank Ghana LTD
**Apr 2024 - Present** | Accra, Ghana

**DevOps Engineering Lead** | Apr 2024 - Present

- Founded the bank's DevOps team of 4 engineers, replacing manual code handoffs with enforced Git workflows, containerized Kubernetes deployments, and automated release pipelines.
- Implemented CI/CD automation using Azure DevOps and GitHub Actions that cut deployment time by ~90% and increased release velocity ~5x; introduced GitOps with FluxCD for consistent repeatable deployments; integrated Veracode and Trivy scanning for automated security analysis.
- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests, with 99.97% measured uptime inclusive of monthly scheduled maintenance.
- Managed multi-cloud infrastructure across Azure and AWS: resource provisioning, private VPC peering to on-prem systems, deployments, IAM, access control, and cost optimization.
- Automated 95% of infrastructure configuration management using Ansible, Python, and Bash, turning multi-day manual processes into reproducible, version-controlled deployments.
- Introduced a unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting, reducing mean time to resolution on production incidents.

**Team Lead, Core Banking Services** | May 2025 - Present

- Own the on-prem Finacle core banking deployment on Tanzu Kubernetes Grid, managing deployments, patching, and incident response across 800+ production pods to sustain 1.5M+ daily transactions.
- Extended the bank's observability stack into core banking with Finacle-specific dashboards for CPU/memory trends, transaction volumes, response times, and exceptions, plus threshold-based alerting for proactive scaling.
- Built a bank-wide OTP service using Django (Python) and Next.js, integrating SMS and email gateways, to secure core banking access for 600+ internal users with structured logging to Elasticsearch via Filebeat.
- Built a national ID verification service using Django (Python) and Next.js, processing and storing ID documents in self-hosted MinIO with automated verification and customer record updates.
- Led a 5-person QA team through the bank's Basis-to-Finacle migration cutover, designing and executing 10,000+ test cases across 13 core banking modules and 33 internal applications over a two-week window.
- Architected integrations between Finacle core banking and third-party systems including transaction portals and internal tools.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024

- Designed secure, cost-efficient AWS infrastructure running containerized microservices on EKS and ECS with autoscaling, load balancing, and inter-service communication.
- Automated application delivery and infrastructure provisioning via CI/CD pipelines on GitHub Actions and Terraform, making deployments repeatable, auditable, and reversible.
- Designed a disaster recovery strategy mirroring the AWS production environment on GCP using GKE, Cloud SQL, and Cloud Storage, with secure VPCs, IAM policies, and dual-environment CI/CD for rapid failover.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS/SNS, with SMS, email, and payment provider integrations including multi-provider failover.
- Led performance optimizations that reduced peak request latency by 90% through Redis caching, query tuning, and indexing in PostgreSQL.
- Architected the myhealthcop.com platform end-to-end, delivering three applications: a patient-facing Flutter mobile app, a Flutter app for health professionals, and a React admin dashboard.
- Led a 12-person cross-functional team through full project lifecycle under Agile/Scrum.

---

## Projects

### Virk Cloud (virk.cloud)
**Founder & CTO** | Aug 2025 - Present

- Architected a multi-tenant Platform-as-a-Service for startups with built-in CI/CD, fixed billing, observability, real-time log streaming, and alerting.
- Built the full management console in Next.js with authentication, user management, real-time monitoring dashboards, and billing.
- Manage the underlying infrastructure on virtual private servers: RKE2 cluster deployment, hardware/storage provisioning, network and traffic management, and DNS.
- **Stack:** Kubernetes (RKE2), Terraform, FluxCD, Prometheus, Grafana, Next.js, Convex, Python

### AI Agents for Infrastructure Operations
**Personal R&D** | 2024 - Present

- Building specialized AI agents for QA automation, code review, and sysadmin operations, running against live Linux production servers with real workloads.
- Prototyping agent-driven SaaS tools using RAG, tool-use, and multi-agent orchestration patterns.
- Completed AI Engineering Specialization (ByteByteAI) covering agents, RAG, and LLM application development.

### Digital-Recon: Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Building a real-time transaction reconciliation engine for financial institutions, detecting discrepancies across heterogeneous data sources including relational DBs, REST APIs, Elasticsearch, and Kafka topics.
- Architected an event-driven processing layer using Kafka for upstream transaction ingestion and Celery for scheduled and on-demand reconciliation jobs, including windowed scans, per-source reprocessing, and downstream alerting.
- Designed a Next.js/TypeScript triage dashboard enabling operators to define reconciliation rules and resolve mismatches with a full audit trail.
- **Stack:** Kafka, Celery, Python, Elasticsearch, PostgreSQL, Docker, Next.js, TypeScript

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
