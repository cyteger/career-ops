 <!-- career-ops:render format=letter language=en company="Bitovi" date=2026-04-12 number=001 -->
# Oswald Gyabaah

**AI-Enabled Full-Stack Engineer & Platform Builder**

oswald.gyabaah@gmail.com | +233 55 413 4307 | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana (GMT+0, full US Central overlap)

---

## Professional Summary

Full-stack engineer with 6 years shipping production web and mobile applications end to end across React/Next.js frontends, Node.js/Python backends, and Kubernetes infrastructure. Fluent in JS-based metaframeworks, component architecture, and state management, with active practice in AI-assisted development (Claude Code, Cursor) and production AI agent systems for QA and infrastructure operations. Founding CTO at MyHealthCop (12-person cross-functional team, 3 shipped apps on AWS/GCP) and founder of GTBank Ghana's DevOps practice (CI/CD cut deployment time ~90%, 99.97% uptime on 3M+ daily requests). Based in Accra, with full overlap with US Central business hours. Portfolio: github.com/cyteger.

---

## Core Competencies

- Fullstack JavaScript / TypeScript (React, Next.js, Node.js)
- AI-Assisted Development (Claude Code, Cursor, agentic workflows)
- Component Architecture & Metaframeworks
- State Management Patterns (Hooks, Convex, Redux-style)
- CI/CD Pipelines & GitOps (FluxCD, GitHub Actions, ArgoCD)
- Codebase Audits & Performance Tuning
- Deployment & Infrastructure Best Practices
- Client Consulting & Engineer Coaching

---

## Technical Skills

- **Frontend:** React, Next.js (SSR/SSG), TypeScript, JavaScript, Tailwind CSS, component architecture (HOC/Render Props/Hooks), design system patterns, responsive UI
- **Backend:** Node.js (Express), Python (Django, FastAPI, Celery), REST, GraphQL, WebSockets, secure service layers
- **State & Real-time:** Hooks-based state, Convex real-time subscriptions, WebSockets, Firebase Realtime, Server-Sent Events
- **AI Development:** Claude API, OpenAI API, RAG systems, multi-agent orchestration, tool-use patterns, AI-assisted development workflows (Claude Code, Cursor)
- **Mobile:** Flutter (iOS + Android, shipped to App Store + Play Store), React Native fundamentals
- **Databases:** PostgreSQL, MySQL, MongoDB, Firebase/Firestore, Convex, SQLite, Redis
- **Messaging & Orchestration:** AWS SQS/SNS, RabbitMQ, Redis queues, Kafka, Celery workers (Temporal-adjacent patterns)
- **Testing:** Jest, React Testing Library, Playwright E2E, Cypress, pytest, UAT coordination
- **CI/CD & IaC:** GitHub Actions, Azure DevOps, FluxCD, ArgoCD, Terraform, Ansible, Codemagic
- **Cloud & Containers:** AWS (EKS, ECS, S3, SQS/SNS, VPC), GCP (GKE, Cloud SQL, Cloud Storage), Azure, Kubernetes, Docker, Helm
- **Observability:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry
- **Security:** OAuth2 (Keycloak), OIDC, JWT, 2FA/OTP, Veracode, Trivy, TLS/SSL
- **Deployment Platforms:** Vercel, Virk Cloud (self-built PaaS), Firebase Hosting, self-hosted K8s

---

## Professional Experience

### Team Lead, Core Banking Operations
**Guaranty Trust Bank Ghana LTD** | May 2025 - Present

- Designed and shipped a bank-wide 2FA / OTP verification service: **Next.js** frontend + Django API backend with SMS/email gateway integrations, logging to Elasticsearch via Filebeat, securing core banking logins for 600+ internal users
- Built a Ghana Card ID verification tool (**Next.js + Python/Celery + Redis**): processes national ID verification for bank customers, stores documents in self-hosted MinIO, updates customer records with verified image links
- Led end-to-end QA for the bank's migration from Basis to Finacle core banking: planned and executed 10,000+ test cases across 13 modules and 33 applications, coordinating integration, UAT, and peripheral device validation
- Architected multi-system integrations between Finacle core banking and internal applications (transaction portals, internal tools, peripheral services)
- Manage the Finacle Services team running core banking on TKG Kubernetes: 800+ production pods and full lifecycle covering deployments, patching, and incident response, sustaining 1.5M+ daily banking transactions
- Built the observability stack with dashboards tracking CPU/memory trends, transaction volumes, response times, and categorized exceptions, enabling threshold-based alerting and proactive scaling

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 - May 2025 | Accra, Ghana

- Founded the bank's DevOps team of 4 engineers and coached junior engineers through modern delivery practices: Kubernetes, containerized deployments, disciplined version control, and automated release workflows
- Implemented **CI/CD automation** that cut deployment time by ~90% and increased release velocity ~5x; introduced **GitOps with FluxCD** for consistent, repeatable deployments; integrated Veracode and Trivy for automated security analysis
- Architected high-availability Kubernetes clusters handling 3M+ daily requests with 99.97% uptime SLA; implemented auto-scaling and self-healing mechanisms
- Automated 95% of infrastructure configuration management using Ansible, Python, and Bash, transforming multi-day manual processes into reproducible, version-controlled deployments in minutes
- Introduced a unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting to accelerate RCA
- Managed multi-cloud infrastructure across Azure and AWS: provisioning, private VPC links to on-prem systems, access control, cost optimization, and reliable operation of GTExpress and GTWorld

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024

- Architected the full myhealthcop.com platform **end to end** across requirements, system design, database modeling, and API architecture, delivering three shipped applications: patient-facing web portal (**React**), Flutter mobile app (iOS + Android, in App Store and Play Store), and admin management dashboard (**React**)
- **Recruited and managed a 12-person cross-functional team**: 2 frontend (React), 3 backend (incl. self), 2 mobile (Flutter), 2 product, 2 designers, 1 QA
- Designed secure, cost-efficient AWS infrastructure orchestrating containerized microservices on EKS and ECS with autoscaling, load balancing, and seamless inter-service communication
- Built a high-throughput background processing system handling **1M+ daily jobs** (payments, messaging, notifications) on SQS/SNS with provider failover, applying a Temporal-adjacent durable execution pattern
- **Reduced peak latency by 90%** through PostgreSQL query tuning, Redis caching, and strategic indexing
- Automated infrastructure provisioning with Terraform and built CI/CD pipelines to streamline deployments and minimize human errors
- Designed and implemented disaster recovery: parallel GCP production environment mirroring AWS on GKE + Cloud SQL + Cloud Storage, with dual-environment CI/CD for rapid failover
- Managed full project lifecycle across Agile/Scrum: requirements, sprint planning, stakeholder management, risk assessment, budgeting, delivery

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

### Virk Cloud: virk.cloud
**Founder & CTO** | Aug 2025 - Present

- Architected a production-grade Kubernetes PaaS (comparable to Vercel) that lets startups deploy clusters instantly without operational overhead, with fixed billing, built-in observability, real-time log streaming, and alerts
- Built the full management console in **Next.js** with authentication, cluster management, real-time monitoring dashboards, billing, and state management, deployed on the platform itself (dogfooded)
- Manage infrastructure on virtual private servers: cluster deployment (RKE2), storage provisioning, network/traffic management, DNS
- Automated every deployment using FluxCD and Terraform for reproducible, version-controlled operations
- **Stack:** Next.js, TypeScript, Tailwind CSS, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana

### Vistara: Property Tenant Assessment Platform
**Founder** | 2025 - Present

- Multi-app platform helping renters evaluate housing conditions (water, electricity, safety, noise) before signing leases
- Built landing page, tenant web app (assessment form), admin web dashboard, and admin mobile app (Flutter) for field data collection
- Currently in TestFlight (iOS) with web version live
- **Stack:** Next.js, React, TypeScript, Flutter, Codemagic CI/CD

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana

---

## Professional Certifications

- AI Engineering Specialization (ByteByteAI): Agents, RAG, LLM applications
- Certified Oracle DevOps Professional
- Certified Oracle Cloud Solutions Architect Associate

---

## Writing & Community

- **risingEngineers** (Substack): technical blog on software engineering and infrastructure
- **Digital-Recon**: real-time transaction reconciliation engine for financial institutions (React + Python + Celery + Kafka + Elasticsearch)
- **GTBank DevOps**: trained and mentored 3 junior engineers in Kubernetes, CI/CD, and GitOps practices
- **MyHealthCop**: built and led a 12-person cross-functional engineering organization from zero
