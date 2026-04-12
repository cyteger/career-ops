# Oswald Gyabaah

**Full-Stack Software Engineer & DevOps Lead**

oswald.gyabaah@gmail.com | +233 55 413 4307 | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

Full-stack engineer with 6 years building, shipping, and scaling production systems end-to-end -- from React/Next.js frontends to Python/Node backends to Kubernetes infrastructure. Led a 12-person cross-functional team as founding CTO (MyHealthCop), founded GTBank Ghana's DevOps practice from scratch, and now builds AI agents for infrastructure automation and QA. Equally strong in Python and JavaScript/TypeScript. Ships across web (React, Next.js), mobile (Flutter, iOS + Android), backend (Django, FastAPI, Node.js), and infrastructure (Kubernetes, Terraform, multi-cloud). Currently building AI-powered SaaS products using RAG, tool-use, and multi-agent orchestration patterns.

---

## Technical Skills

- **Frontend:** React, Next.js (SSR/SSG), TypeScript, JavaScript, Tailwind CSS, HOC/Render Props/Hooks patterns, component architecture, responsive design
- **Mobile:** Flutter (iOS + Android, published to App Store + Play Store), React Native fundamentals
- **Backend:** Python (Django, FastAPI, Celery), Node.js (Express), REST APIs, GraphQL, WebSockets
- **Databases:** PostgreSQL, MySQL, MongoDB, Firebase/Firestore, Convex, SQLite, Redis
- **Real-time:** Convex real-time subscriptions, WebSockets, Firebase Realtime, Server-Sent Events
- **Messaging & Queues:** AWS SQS/SNS, RabbitMQ, Redis queues, Kafka, Convex cron jobs
- **Testing:** Jest, React Testing Library, Cypress, Playwright E2E, pytest, UAT coordination
- **Cloud & Infrastructure:** AWS (EKS, ECS, S3, SQS/SNS, VPC), GCP (GKE, Cloud SQL, Cloud Storage), Azure, OCI, VMware, on-prem bare metal (Tier III data centers)
- **Container Orchestration:** Kubernetes (EKS, GKE, TKG/Tanzu, RKE2), Docker, Helm, Istio Service Mesh
- **CI/CD & GitOps:** Terraform, Ansible, GitHub Actions, ArgoCD, FluxCD, Azure DevOps, Codemagic
- **Observability:** Prometheus, Grafana, ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat), Sentry
- **Security & Auth:** OAuth2 (Keycloak), OIDC, JWT, LDAP, 2FA/OTP systems, Veracode, Trivy, IPSec/OpenVPN, TLS/SSL, WAF
- **AI & Agents:** LLM API integration (Claude, OpenAI), RAG systems, AI agent development, multi-agent orchestration, tool-use patterns, AI-assisted development workflows
- **Architecture:** Microservices design, API design, database modeling, enterprise system integration, disaster recovery planning, multi-cloud architecture
- **Project Management:** Full project lifecycle (requirements through delivery), Agile/Scrum, Kanban, stakeholder management, risk assessment
- **Tools:** Git, GitHub, Azure DevOps, Notion, Jira, Linear, Plane, MinIO (self-hosted object storage)
- **Deployment Platforms:** Vercel, Virk Cloud (self-built PaaS), Firebase Hosting, self-hosted K8s on-prem

---

## Professional Certifications

- AI Engineering Specialization (ByteByteAI) -- Agents, RAG, LLM applications
- Certified Oracle DevOps Professional
- Certified Oracle Cloud Solutions Architect Associate

---

## Professional Experience

### Manager, Finacle Services Team
**Guaranty Trust Bank Ghana LTD** | May 2025 - Present

- Manage the Finacle Services team running the on-prem core banking system on Tanzu Kubernetes Grid (TKG), overseeing 800+ production pods and the full cluster lifecycle: deployments, patching, and incident response, sustaining 1.5M+ daily banking transactions
- Led end-to-end QA for the bank's migration from Basis to Finacle: planned and executed 10,000+ test cases across 13 core banking modules and 33 internal applications, coordinating integration, UAT, and peripheral device validation
- Built the observability stack with dashboards tracking CPU/memory trends, transaction volumes, response times, and categorized exceptions -- enabling threshold-based alerting and proactive scaling
- Lead L2 support operations, correlating transactional and application logs across interfaces and core banking microservices via the Elastic Stack, driving root-cause analysis and cross-functional remediation
- Architected multi-system integration between Finacle core banking and third-party applications: transaction portals, internal tools, and peripheral services
- Designed and deployed a bank-wide second factor verification service (OTP): Next.js frontend + Django API backend with SMS/email gateway integrations, logging to Elasticsearch via Filebeat, securing core banking logins for 600+ internal users
- Built a Ghana Card verification tool (Next.js + Python/Celery + Redis): processes national ID verification for bank customers, stores documents in self-hosted MinIO, and updates customer records with verified ID card image links

### DevOps Engineering Lead
**Guaranty Trust Bank Ghana LTD** | Apr 2024 -- May 2025 | Accra, Ghana

- Founded the bank's DevOps team of 4 engineers, leading junior engineers to establish modern delivery practices -- introducing Kubernetes, containerized deployments, disciplined version control, and automated release workflows
- Implemented CI/CD automation that cut deployment time by ~90% and increased release velocity ~5x; introduced GitOps with FluxCD for consistent repeatable deployments; integrated Veracode and Trivy scanning for automated security analysis
- Architected high-availability Kubernetes clusters across multiple on-prem environments running internal applications handling 3M+ daily requests with 99.97% uptime SLA; implemented auto-scaling and self-healing mechanisms
- Automated 95% of infrastructure configuration management using Ansible, Python, and Bash scripts -- transforming multi-day manual processes into reproducible, version-controlled deployments in minutes
- Implemented stateless, version-controlled cluster deployments with FluxCD, Helm, and Azure DevOps for consistency, idempotency, and rapid disaster recovery cluster rebuilds
- Introduced unified observability stack (Prometheus, Grafana, Elastic Stack, Sentry) for centralized logging, tracing, and real-time alerting to accelerate RCA and improve mean time to resolution
- Managed multi-cloud infrastructure across Azure and AWS: resource provisioning, private VPC links to on-prem systems, deployments, access control, cost optimization, and reliable operation of GTExpress and GTWorld

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 -- Mar 2024

- Founded the technical organization and recruited/managed a 12-person cross-functional team: 2 frontend (React), 3 backend (including self), 2 mobile (Flutter), 2 product managers, 2 designers, 1 QA engineer
- Architected the full myhealthcop.com platform end-to-end: requirements gathering, system design, database modeling, API architecture -- delivering three distinct applications: patient-facing web portal (React), Flutter mobile app (iOS + Android, published to App Store and Play Store), and admin management dashboard (React)
- Designed secure, cost-efficient AWS infrastructure orchestrating containerized microservices using EKS and ECS with autoscaling, load balancing, and seamless inter-service communication
- Built a high-throughput background processing system handling 1M+ daily jobs (payments, messaging, notifications) using SQS/SNS with SMS, email, and payment provider integrations including failover and provider fallback
- Reduced peak latency by 90% through database query tuning, caching layers (Redis), and indexing across PostgreSQL
- Automated infrastructure provisioning with Terraform, reducing setup time by 90% while building CI/CD pipelines to streamline deployments and minimize human errors
- Designed and implemented disaster recovery: parallel GCP production environment mirroring AWS using GKE, Cloud SQL, and Cloud Storage with secure VPCs, IAM policies, and dual-environment CI/CD for rapid failover
- Managed full project lifecycle: requirements gathering, sprint planning, stakeholder management, risk assessment, budgeting, and delivery across Agile/Scrum methodology

---

## Projects

### Palsar — AI Web Monitoring SaaS
**Founder** | 2025 -- Present

- Built an AI-powered web monitoring platform using Claude API that watches websites and alerts users on relevant changes in plain English
- Multiple monitoring modes: fixed URL tracking, AI-discovered URLs, dynamic search-based monitoring with natural language relevance filtering
- Multi-channel notifications with configurable alert rules
- **Stack:** Next.js 14, React, TypeScript, Convex (real-time backend), Anthropic Claude API, Vercel

### Root-ID — AI Agent Identity & Messaging Platform
**Founder** | 2025 -- Present

- Designed an identity, discovery, and async messaging platform for AI agents across organizations -- agent registry with cryptographic verification and message inbox without requiring live API connections
- Planning open-core release for the developer community
- **Stack:** Next.js (React 19), TypeScript, Convex (real-time), Playwright E2E tests, Vercel

### Digital-Recon — Transaction Reconciliation Engine
**Founder** | 2025 -- Present

- Built a real-time transaction reconciliation engine for financial institutions that detects discrepancies across multiple data sources (databases, APIs, Elasticsearch, Kafka)
- Web dashboard for triage and resolution of transaction mismatches across disparate banking systems
- **Stack:** React, TypeScript, Python, Docker, PostgreSQL, Kafka, Elasticsearch

### Virk Cloud — virk.cloud
**Founder & CTO** | Aug 2025

- Architected a production-grade Kubernetes PaaS (comparable to Vercel) enabling startups to deploy clusters instantly without operational overhead -- fixed billing, built-in observability, real-time log streaming, and alerts
- Built the full management console in Next.js: authentication, cluster management, real-time monitoring dashboards, billing, state management -- deployed on the platform itself
- Manage full infrastructure on virtual private servers: cluster deployment (RKE2), hardware/storage provisioning, network/traffic management, DNS maintenance
- Automated all deployments using FluxCD and Terraform for reproducible, version-controlled operations
- **Stack:** Next.js, TypeScript, Tailwind CSS, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana

### Vistara — Property Tenant Assessment Platform
**Founder** | 2025 -- Present

- Multi-app platform helping renters evaluate housing conditions (water, electricity, safety, noise) before signing leases
- Built landing page, tenant web app (assessment form), admin web dashboard, and admin mobile app (Flutter) for field data collection
- Currently in TestFlight (iOS) with web version hosted
- **Stack:** Next.js, React, TypeScript, Flutter, Codemagic CI/CD

### AI Agents for Infrastructure Operations
**Personal R&D** | 2024 -- Present

- Building specialized AI agents for QA automation, code review, and sysadmin operations on production Linux servers -- fully operational against real systems
- Developing agent-driven SaaS products leveraging RAG, tool-use, and multi-agent orchestration patterns
- Completed AI Engineering Specialization (ByteByteAI) covering agents, RAG, and LLM application development

### Education Research and Innovation Foundry — erifoundry.org
**Founder & Research Lead** | Oct 2025 -- Present

- Leading design of AI-driven research initiatives in adaptive learning, cognitive modeling, and educational analytics
- Coordinating cross-disciplinary research to develop experimental frameworks for scalable ML and software solutions in education
- Prototyping applications of LLMs in human-centered learning systems

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 -- May 2020 | Berekuso, Ghana

---

## Writing & Community

- **risingEngineers** (Substack) -- Technical blog on software engineering and infrastructure
- **Root-ID** -- Planned open-core release for AI agent identity infrastructure
- **GTBank DevOps** -- Trained and mentored 3 junior engineers in Kubernetes, CI/CD, and GitOps practices
- **MyHealthCop** -- Built and led a 12-person cross-functional engineering organization from zero
