<!-- career-ops:render format=a4 language=en company="accelerayt" date=2026-04-22 number=006 -->
# Oswald Gyabaah

**Senior Full-Stack Engineer — Vue/React, Node.js, AWS Serverless (Lambda, DynamoDB, CloudFormation)**

oswald.gyabaah@gmail.com | +233 55 413 4307 | [linkedin.com/in/ogyabaah](https://linkedin.com/in/ogyabaah) | [github.com/cyteger](https://github.com/cyteger) | Accra, Ghana

---

## Professional Summary

Senior full-stack JavaScript engineer with 6 years shipping production systems end-to-end: React/Next.js and Vue-style reactive frontends, Node.js and Python backends, and AWS serverless infrastructure (Lambda, DynamoDB, CloudFormation, API Gateway). Founded MyHealthCop as CTO and delivered three apps plus AWS/GCP infrastructure with 1M+ daily background jobs. At GTBank Ghana, took over an in-flight core banking platform and now operate 800+ production pods at 99.97% uptime with 1.5M+ daily transactions. Comfortable inheriting live codebases, evolving them with minimal hand-holding, and shipping from day one. Strong async communication; steady, low-drama operator.

---

## Professional Certifications

- AI Engineering Specialization (ByteByteAI), Mar 2026: Agents, RAG, LLM applications
- Oracle Certified DevOps Professional (Oracle), Aug 2025
- Oracle Certified Architect Associate (Oracle), Aug 2025
- Oracle Certified Foundations Associate (Oracle), Jul 2025
- AWS Certified Cloud Practitioner (AWS), May 2024
- Django Web Framework (Coursera), Dec 2022

---

## Technical Skills

- **Frontend:** JavaScript, TypeScript, React.js, Next.js, Vue-adjacent reactive patterns, Tailwind CSS, Flutter (mobile)
- **Backend:** Node.js (Express, Lambda handlers), Python (Django, FastAPI, Celery), REST APIs, GraphQL, WebSockets
- **AWS Serverless:** Lambda, DynamoDB (single-table design), API Gateway, CloudFormation, SQS/SNS, S3, CloudWatch, X-Ray, IAM, KMS, Secrets Manager
- **AWS Broader:** EKS, ECS, VPC networking, private links, cost optimization and billing analysis
- **Other Cloud & Infra:** GCP (GKE, Cloud SQL, Cloud Storage), Azure, OCI, Kubernetes (EKS, GKE, TKG, RKE2), Terraform, Ansible, Helm
- **Databases:** DynamoDB, PostgreSQL, MongoDB, MySQL, Firebase/Firestore, Redis, Convex
- **CI/CD & GitOps:** GitHub Actions (incl. serverless deploys), FluxCD, ArgoCD, Azure DevOps, Codemagic
- **Observability:** CloudWatch, X-Ray, Prometheus, Grafana, ELK Stack, Sentry
- **Testing:** Jest, React Testing Library, Playwright E2E, Cypress, pytest, UAT coordination

---

## Professional Experience

### Guaranty Trust Bank Ghana LTD
**Apr 2024 - Present** | Accra, Ghana

**Team Lead, Core Banking Services** | May 2025 - Present

- Took over an in-flight Finacle deployment on Tanzu Kubernetes Grid (TKG) mid-migration — read the existing configuration, onboarded the team, and shipped without a long ramp-up. Now operate 800+ production pods sustaining 1.5M+ daily transactions.
- Led a 5-person QA team through the Basis-to-Finacle core banking migration cutover, executing 10,000+ test cases across 13 modules and 33 applications in a two-week window (integration, UAT, peripheral device validation).
- Built a bank-wide OTP service (Next.js + Node.js API + Django), integrating SMS and email gateways to secure core banking access for 600+ internal users.
- Extended observability into core banking with Finacle-specific dashboards and threshold-based alerting for proactive scaling.
- Collaborated with product and risk stakeholders to scope, estimate, and deliver integrations between core banking and third-party systems.

**DevOps Engineering Lead** | Apr 2024 - Present

- Founded the bank's DevOps team of 4 engineers from zero and introduced enforced Git workflows, containerized deployments, and automated release pipelines — replacing manual code handoffs.
- Implemented CI/CD automation on GitHub Actions and Azure DevOps that cut deployment time ~90% and increased release velocity ~5x, with Veracode and Trivy scanning on every merge.
- Architected HA Kubernetes clusters handling 3M+ daily requests at 99.97% measured uptime, with auto-scaling and self-healing.
- Managed multi-cloud AWS and Azure infrastructure: resource provisioning, private VPC links, access control, and cost optimization.

### Chief Technical Officer (Founding)
**MYHEALTHCOP LTD** | Jan 2021 - Mar 2024 | Accra, Ghana

- Architected the myhealthcop.com platform end-to-end across requirements, system design, data modelling (PostgreSQL + DynamoDB for high-volume event data), and API development — delivering a patient Flutter app, a provider Flutter app, and a React admin dashboard.
- Built AWS serverless services for high-throughput workloads: Lambda functions behind API Gateway, DynamoDB with single-table patterns for audit and notification data, and SQS/SNS handling 1M+ daily background jobs across payments, messaging, and notifications with multi-provider failover.
- Wrote Infrastructure as Code on CloudFormation and Terraform for repeatable, auditable, reversible deployments across Dev/Staging/Prod on GitHub Actions CI/CD.
- Designed a multi-cloud disaster recovery strategy mirroring AWS onto GCP (GKE, Cloud SQL, Cloud Storage) with secure VPCs, IAM, and dual-environment CI/CD for rapid failover.
- Cut peak request latency by 90% through Redis caching, DynamoDB access-pattern tuning, and PostgreSQL query optimisation.
- Led a 12-person cross-functional team (frontend, backend, mobile, product, design, QA) through full project lifecycle under Agile/Scrum.

---

## Projects

### Virk Cloud (virk.cloud) — Developer Platform
**Founder & CTO** | Aug 2025 - Present

- Architected a Platform-as-a-Service for startups with built-in CI/CD, fixed billing, real-time log streaming, and alerting.
- Built the full management console in Next.js with authentication, user management, real-time monitoring, and billing.
- Manage the underlying RKE2 Kubernetes cluster, hardware/storage, network and DNS.
- **Stack:** Next.js, JavaScript/TypeScript, Node.js, Convex, Tailwind CSS, Kubernetes (RKE2), FluxCD, Terraform, Prometheus, Grafana

### Vistara — Property Tenant Assessment Platform
**Founder** | 2026 - Present

- Multi-app platform for renters to evaluate housing (water, electricity, safety, noise) before signing leases — landing page, tenant web app, admin dashboard, admin mobile app.
- iOS app in TestFlight; web apps deployed to beta.
- **Stack:** Next.js, React, TypeScript, Node.js API routes, Flutter, Codemagic CI/CD

### AI Agents for Infrastructure Operations
**Personal R&D** | 2024 - Present

- Building specialized AI agents for QA automation, code review, and sysadmin operations against live Linux production servers.
- Prototyping agent-driven SaaS tools using RAG, tool-use, and multi-agent orchestration.
- Completed AI Engineering Specialization (ByteByteAI) covering agents, RAG, and LLM application development.

---

## Education

**Ashesi University** | BSc Computer Engineering | Sep 2016 - May 2020 | Berekuso, Ghana
