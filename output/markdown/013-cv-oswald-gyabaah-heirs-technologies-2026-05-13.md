<!-- career-ops:render format=a4 language=en company="heirs-technologies" date=2026-05-13 number=013 -->
# Oswald Gyabaah

**Solutions Architect and Platform Engineer**

+233 55 413 4307 | oswald.gyabaah@gmail.com | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | Accra, Ghana

---

## Professional Summary

Six years architecting and building web platforms end to end. Founded MyHealthCop as CTO and designed the full platform across three apps, AWS infrastructure, and a multi-cloud disaster recovery strategy on GCP. Founded GTBank Ghana's DevOps practice and now run the on-prem Kubernetes platform behind 1.5M+ daily core banking transactions on 800+ pods at 99.97% uptime. Comfortable bridging stakeholders and engineering because I have led both sides.

---

## Core Competencies

- End-to-end web application architecture
- Multi-cloud design (AWS, GCP, Azure, OCI)
- Microservices, event-driven, and serverless patterns
- API design and integration architecture (REST, GraphQL, WebSockets)
- Database architecture (Postgres, Redis, MongoDB, DynamoDB)
- Security, observability, and disaster recovery design
- Cross-functional team leadership and stakeholder communication

---

## Technical Skills

- **Cloud and Infrastructure:** AWS (EKS, ECS, Lambda, S3, SQS/SNS, EventBridge, DynamoDB, VPC), GCP (GKE, Cloud SQL, Cloud Storage), Azure, OCI, on-prem bare metal
- **Architecture Patterns:** Microservices, event-driven, serverless, multi-region disaster recovery, integration gateways, idempotent processing
- **Containers and Orchestration:** Kubernetes (EKS, GKE, TKG, RKE2), Docker, Helm, Istio
- **Languages and Frameworks:** TypeScript, JavaScript, Python (Django, FastAPI, Celery), Node.js (Express), Next.js, React, Flutter, Tailwind
- **APIs and Messaging:** REST, GraphQL, WebSockets, AWS SQS/SNS, EventBridge, Kafka, RabbitMQ
- **Databases:** PostgreSQL, MySQL, MongoDB, Firebase, DynamoDB (single-table and multi-table), Redis, Convex
- **CI/CD and IaC:** Terraform, Ansible, GitHub Actions, FluxCD, ArgoCD, Azure DevOps
- **Observability and Security:** Prometheus, Grafana, ELK Stack, Sentry, OAuth2, OIDC, Keycloak, JWT, LDAP, Veracode, Trivy

---

## Professional Certifications

- Oracle Certified Architect Associate (Oracle), Aug 2025
- Oracle Certified DevOps Professional (Oracle), Aug 2025
- AWS Certified Cloud Practitioner (AWS), May 2024
- AI Engineering Specialization (ByteByteAI), Mar 2026

---

## Professional Experience

### Core Banking Services Lead
**Guaranty Trust Bank Ghana LTD** | May 2025 - Present | Accra, Ghana

- Architect integrations between Finacle core banking and third-party systems including transaction portals and internal tools, with versioned APIs and audit-grade logging.
- Designed and built a bank-wide OTP service (Next.js + Django) integrating SMS and email gateways for 600+ internal users, with structured logging to Elasticsearch via Filebeat.
- Designed a national ID verification service (Next.js + Django) processing and storing ID documents in self-hosted MinIO with automated verification and customer record updates.
- Own the on-prem Finacle core banking deployment on Tanzu Kubernetes Grid: deployments, patching, and incident response across 800+ production pods sustaining 1.5M+ daily transactions.
- Lead L2 support, correlating logs across internal apps and core banking microservices via the Elastic Stack for root cause analysis.

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 - Present | Accra, Ghana

- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests with 99.97% measured uptime.
- Founded the bank's DevOps team of 4 engineers from zero; brought all 4 to on-call competence within 90 days.
- Implemented CI/CD that cut deployment time by 90% and increased release velocity 5x; introduced GitOps with FluxCD; integrated Veracode and Trivy for automated security scanning.
- Introduced a unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralised logging, tracing, and real-time alerting.
- Automated 95% of infrastructure configuration management using Ansible, Python, and Bash, replacing multi-day manual processes with reproducible deployments in minutes.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Architected the myhealthcop.com platform end to end across requirements gathering, system design, database modelling, and API development. Delivered three apps: a patient Flutter app (iOS + Android), a Flutter app for health professionals, and a React admin web dashboard.
- Designed secure AWS infrastructure running containerised microservices on EKS and ECS alongside Lambda functions for event-driven workloads, with autoscaling, load balancing, and inter-service communication.
- Designed a disaster recovery strategy mirroring the AWS production environment on GCP using GKE, Cloud SQL, and Cloud Storage, with secure VPCs, IAM policies, and dual-environment CI/CD for rapid failover.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS and SNS, with multi-provider failover for SMS, email, and payment providers.
- Led performance optimisations that reduced peak request latency by 90% through Redis caching, query tuning, and PostgreSQL indexing.
- Led a 12-person cross-functional team (frontend, backend, mobile, product, design, QA) under Agile/Scrum.

---

## Projects

### Virk Cloud - Platform-as-a-Service
**Founder and CTO** | Aug 2025 - Present

- Architected a PaaS for startups with built-in CI/CD, observability, and log streaming. Manage underlying RKE2 Kubernetes infrastructure on private VPS.
- **Stack:** Next.js, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana

### Digital-Recon - Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Real-time transaction reconciliation engine for financial institutions. Detects discrepancies across heterogeneous data sources (relational DBs, APIs, Elasticsearch) using Kafka for ingestion and Celery for scheduled and on-demand reconciliation jobs.
- **Stack:** React, TypeScript, Python, Celery, Kafka, Elasticsearch, PostgreSQL

### Vistara - Property Tenant Assessment Platform
**Founder** | 2026 - Present

- Multi-app platform helping renters evaluate housing conditions before signing leases. Built landing page, tenant web app, admin web dashboard, and admin Flutter mobile app for field data collection.
- **Stack:** Next.js, React, TypeScript, Flutter, Codemagic CI/CD

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
