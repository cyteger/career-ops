<!-- career-ops:render format=a4 language=en company="nsano" date=2026-05-13 number=012 -->
# Oswald Gyabaah

**Observability and SRE Lead**

+233 55 413 4307 | oswald.gyabaah@gmail.com | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | Accra, Ghana

---

## Professional Summary

SRE and platform engineer with 6 years operating production systems at scale in banking and fintech. Built and runs the observability stack behind 1.5M+ daily core banking transactions on 800+ Kubernetes pods at 99.97% measured uptime. Founded GTBank Ghana's DevOps practice from zero. Comfortable owning the full observability surface area: metrics, logs, traces, alerting, dashboards, incident response, and post-mortems.

---

## Core Competencies

- Observability strategy and tooling (Prometheus, Grafana, ELK, Sentry)
- Incident detection, response, and root cause analysis
- Production reliability for fintech and banking workloads
- Capacity planning and performance optimisation
- Cross-team partnership with engineering, security, and product
- Mentoring and uplifting on-call engineers

---

## Technical Skills

- **Observability:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry, threshold and anomaly-based alerting, custom dashboards, structured logging, log correlation
- **Cloud and Infrastructure:** AWS (EKS, ECS, Lambda, S3, SQS/SNS), GCP (GKE, Cloud SQL), Azure, OCI, on-prem bare metal (Tier III data centres)
- **Containers and Orchestration:** Kubernetes (TKG, EKS, GKE, RKE2), Docker, Helm, Istio
- **CI/CD and IaC:** Terraform, Ansible, GitHub Actions, FluxCD, ArgoCD, Azure DevOps
- **Languages:** Python (Django, FastAPI, Celery), Bash, TypeScript, JavaScript, Node.js
- **Databases and Messaging:** PostgreSQL, Redis, MongoDB, Kafka, RabbitMQ, AWS SQS/SNS

---

## Professional Certifications

- Oracle Certified DevOps Professional (Oracle), Aug 2025
- Oracle Certified Architect Associate (Oracle), Aug 2025
- AWS Certified Cloud Practitioner (AWS), May 2024
- AI Engineering Specialization (ByteByteAI), Mar 2026

---

## Professional Experience

### Core Banking Services Lead
**Guaranty Trust Bank Ghana LTD** | May 2025 - Present | Accra, Ghana

- Extended the bank's observability stack into core banking with Finacle-specific dashboards covering CPU and memory trends, transaction volumes, response times, and exceptions, plus threshold-based alerting that drives proactive scaling.
- Lead L2 support operations: correlate logs across internal apps and Finacle microservices via the Elastic Stack for root cause analysis and remediation.
- Own the on-prem Finacle deployment on Tanzu Kubernetes Grid: deployments, patching, and incident response across 800+ production pods sustaining 1.5M+ daily transactions.
- Led a 5-person QA team through the bank's Basis-to-Finacle migration cutover, designing and executing 10,000+ test cases across 13 core banking modules and 33 internal applications over a two-week window.
- Built a bank-wide OTP service (Next.js + Django) for 600+ internal users with structured logging to Elasticsearch via Filebeat.

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 - Present | Accra, Ghana

- Introduced a unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralised logging, tracing, and real-time alerting. Reduced mean time to resolution on production incidents.
- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests with 99.97% measured uptime; implemented auto-scaling and self-healing.
- Founded the bank's DevOps team of 4 engineers from zero; brought all 4 to on-call competence within 90 days through paired incident response and weekly observability reviews.
- Implemented CI/CD that cut deployment time by 90% and increased release velocity 5x; introduced GitOps with FluxCD for repeatable deployments; integrated Veracode and Trivy for automated security scanning.
- Automated 95% of infrastructure configuration management using Ansible, Python, and Bash, replacing multi-day manual processes with reproducible deployments in minutes.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Designed a disaster recovery strategy mirroring the AWS production environment on GCP using GKE, Cloud SQL, and Cloud Storage, with secure VPCs, IAM policies, and dual-environment CI/CD for rapid failover.
- Built a high-throughput background processing system handling 1M+ daily jobs across payments, messaging, and notifications using SQS and SNS.
- Led performance optimisations that reduced peak request latency by 90% through Redis caching, query tuning, and PostgreSQL indexing.
- Led a 12-person cross-functional team through the full project lifecycle under Agile/Scrum.

---

## Projects

### Virk Cloud — Platform-as-a-Service
**Founder and CTO** | Aug 2025 - Present

- Architected a PaaS for startups with built-in CI/CD, observability, and log streaming. Manage underlying RKE2 Kubernetes infra on private VPS.
- **Stack:** Next.js, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana

### Digital-Recon — Transaction Reconciliation Engine
**Founder** | 2025 - Present

- Real-time transaction reconciliation engine for financial institutions. Detects discrepancies across heterogeneous data sources (relational DBs, APIs, Elasticsearch) using Kafka for ingestion and Celery for scheduled and on-demand reconciliation jobs.
- **Stack:** React, TypeScript, Python, Celery, Kafka, Elasticsearch, PostgreSQL

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
