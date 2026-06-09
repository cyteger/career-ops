# Master CV Questionnaire — Oswald

Answer in prose, in whatever order suits you. The goal is to recall **real work you did but never wrote down** — never to invent. If you did not do something, just say "no" and skip it. If you only remember a rough range, give the conservative end. The top section is the highest-value, so finish that even if you stop early.

## Theme 1 — The missing GTBank TPM / architecture role (highest value)

1. You held a Technical Program Manager role at GTBank (with architecture responsibility) that is not on the CV. What was the official title and the dates? How many teams or workstreams ran through your programs, and which architecture decisions were yours to make versus recommend? How many concurrent projects, and what was your on-time delivery record?
> It was an add on responsibility where I recieve application requests and was responsible for first understanding the requirements, writing the technical requirments and creating the high level architecture and recommend the design and codind approach but those were non-binding and devs could go their own way. Also in charge of UATs to validate what's been done with business users to see if they are satisfied. I worked on about 5 projects before handing over to someone else to focus on Finacle. All projects under my watch were delivered on time. Any further questions you can use the inbuilt questions tool to ask me. 

2. Who did you present to during that role and during the Finacle migration and DR simulations (CIO, CTO, steering committee, auditors, regulator)? Were you on any architecture review board or change advisory board?
> Mainly Developers and Business users along with my group head and occasionally the CIO and CSO for the TPM role. For Finacle migration and DR I presented to the CIO, CSO, Change Advisory board
3. Did you ever write architecture up formally — ADRs, design docs, trade-off write-ups (for example TKG over OpenShift, FluxCD over ArgoCD, GCP for DR)? Roughly how many, and were any signed off above you?
> no
4. When you founded the DevOps practice, did you create reusable templates, golden-path pipelines, or standards other teams had to follow? How many teams or apps adopted them?
> yes devops adoption road maps for developer and application support teams to follow, new git driven standards, deployment runbooks, Azure devops server templates for designing pipelines. Two teams the application development team and the application support team (operations team) a total of about 40 apps an counting

## Theme 2 — Hidden full-stack and product depth

5. Your CV under-represents your full-stack work. Outside MyHealthCop and the side projects, what production full-stack apps have you shipped (React/Next.js, Node, Python, Flutter)? Who used them and at what scale?
> mainly Myhealthcop and side projects along with the 2-fa app bankwide auth service
6. For MyHealthCop: how many users (patients + professionals) did it reach, what payment/transaction volume flowed through it, and what uptime did you deliver? Any funding, partnerships, or a scale milestone?
> I left was it went live was starting to scale so barely 1000 users and about 40+ health professionals. Uptime was excellent. never had any downtimes under my watch as the entire project was on AWS 
7. For Virk Cloud, Digital-Recon, and Vistara: which are live with real traffic/users today, and roughly how many? Which one would you be happiest having a hiring manager open and click around in?
> I would want people to see lodestar.cv the project is located at /Users/oswald.gyabaah/projects/kirates/folio and just went live. The rest are not live yet are WIP
8. Did Digital-Recon come out of a real reconciliation problem at GTBank (settlement breaks between Finacle and GhIPSS/MoMo/the switch, suspense or GL clean-up)? What were you reconciling, and at what volume?
> Yes digital recon was built in direct response to critical problems GTBank faces with transactions getting stuck in ledges, debits for which there was no corresponding credits and vice versa. Failed transfers not auto reversed and needing manual intervention, it was built to handle all of that and more and meant to evolved into a full side kick for the corebanking software handing anything the core banking software doesn't

## Theme 3 — Core banking and payments domain

9. Which payment rails did your Finacle integrations actually touch — GhIPSS (GIP, GhQR, gh-link, e-zwich), mobile money (MTN MoMo, Telecel Cash, AirtelTigo), card/ATM/POS (ISO 8583, a switch like SmartVista or Postilion), RTGS, ACH, or SWIFT? For each, were you on the posting/settlement side or the connectivity/monitoring side?
> We handle: GhIPSS, mobile money, card/ATM/POS, Postilion, RTGS, ACH, SWIFT, OE PAY, along with remittance services like Remitly, Ria, etc. Personally on the monitoring side. The guy the call when swift transactions post via core banking or other standalone solutions are failing to reach swift or Other providers personally not responsible for posting, business users do that. Maintain the applications that integrate with those providers to ensure business users can post
10. What sat between Finacle and the channels/third parties — an ESB (IIB, MuleSoft, WSO2), an API gateway (Kong), Finacle's own Connect/FIC layer, or services you wrote? Which protocols (SOAP/REST, MQ, host-to-host files)?
> Internal REST middleware with own gateway and mnicroservices for branches, accounts, transations, cheques, customers, etc for interacting with various fincale solutions
11. How long was your Finacle EOD/BOD batch window, and did you ever troubleshoot or tune a stuck or overrunning end-of-day cycle (interest accrual, GL handoff, day-end cutover)?
> EOD batch window is about 1HR long and yes occassionally I am called in to fix long running ops that's not going as expected. Resource exhaustion issues, pods scaling and bottle neck, etc
12. On the Oracle DB under Finacle: was the near-zero-RPO DR achieved with Data Guard? How hands-on were you with the Oracle side (RAC, ASM, RMAN backups, log shipping) versus handing it to the DBAs?
> yes data guard realtime replication. I am not on the DB team purely handled by DBAs everything is handed to DBAs they just give me feedback on when to do what or what's going on
13. Which Finacle version and modules did you run (core, FEBA, Connect24, treasury), and on the Basis-to-Finacle migration were you involved in data-migration mapping or Finacle config/scripting, not just QA?
> Finacle 11 full containerized apps. I was not involved in data-migration or scripting purely QA role at first before assuming operation responsibility later
14. Did your platform fall in PCI-DSS scope, did the national-ID verification service feed KYC/AML (sanctions/PEP screening, transaction monitoring), and did any Bank of Ghana directive shape your work (cybersecurity directive, data residency keeping the DR site in-country, regulator-set RTO/RPO)? Did you ever interact with an HSM or key ceremony? Which customer channels ran through your platform (internet banking, mobile app, USSD)?
> Yes bank is subject to PCI DSS scope and autdits. Yes the ghana card verification was mainly for KYC. Yes BoG requires data residency in country but also for DC to be on bank's premise and require DR site to be at least 250km away. Regulator set RPO/RTO my job is compliance. all of internet banking, mobile app, USSD, ATM, POS, etc all run through finacle

## Theme 4 — The operational stack behind the work you already describe

15. Running FluxCD GitOps at a bank, how did you keep secrets out of Git — Sealed Secrets, External Secrets Operator, Vault, SOPS, or cloud KMS — for DB credentials and gateway keys?
> External secret operator using vault
16. How did you handle TLS certificates for the internal apps and ingress — cert-manager, an internal/enterprise CA, or manual rotation? Did you ever enable mTLS between services?
> Public CA from sectigo renewed annually. mTLS in cluster for istio services and the downstream applications. Certs also kept in vault and loaded dynamically by apps like elastic search, harbor, etc. Manual CA rotation when new certs available. 
17. What storage backend sits under your on-prem Kubernetes (vSphere CSI, Longhorn, Ceph/Rook, NFS), and who manages StorageClasses and PVCs for the stateful services?
> NFS drive over the network. I am manage StorageClasses and PVCs for the stateful services Sys admin manages the underlying NFS drive. 
18. For the DR program, how do you actually back up and restore cluster state and persistent data (Velero, etcd snapshots, vSphere/array snapshots, DB-native backups), and how do you test restores?
> Velero. not sure of testing restores. DC/DR clusters are independent of each other and only have applications synced from git between, underlying clusters independent and handled by vmware
19. Which CNI runs on your clusters (Antrea/NSX-T on Tanzu, Calico, Cilium), and did you write NetworkPolicies to segment the banking namespaces? How do you expose services on bare metal (ingress controller plus MetalLB/F5/HAProxy/NSX, and any WAF)?
> Antrea/NSX-T on Tanzu. WAF but I don't maintain, network team does. Ingress controllers with HTTPRoute plus metal LB. Network policies for segmentation
20. How do users and engineers authenticate to clusters and apps — did you wire RBAC and app login into Active Directory/LDAP via OIDC, and run Keycloak, Dex, or ADFS?
> vspere.local user provisioned in vsphere users login via delegated auth. Keycloack for certain apps and Active Dir for others too
21. How much hands-on Linux and networking do you do (systemd, sysctl/kernel tuning, DNS, firewalls, VLANs, routing in the data center)? Have you done vSphere/ESXi admin, provisioned servers/storage, or stood up DR-site hardware?
> No that's sys admin work outside my scope
22. Have you written any Go (a Kubernetes operator/controller, an admission webhook, a Prometheus exporter, a CLI), or has automation stayed in Python and Bash? Did you enforce any cluster policy through admission control (OPA Gatekeeper, Kyverno, Pod Security Standards)? What did you actually do with Istio beyond installing it?
> Admission controller but not in finacle in my own cluster in virk. Istio installation only

## Theme 5 — Numbers we are missing

23. Before vs after you introduced the observability stack and L2 process: roughly how long to detect and resolve a production incident, and how long after? Rough monthly incident count (or Sev1/Sev2), and did it drop?
> most downtimes detected with 90s of occurance through gatus monitoring. Resolution can be sometimes in minutes other might take up a few hours and occasionally days for issues that need escalation. Monthly incidents are anywhere between 0 and 2
24. Do you run against a formal uptime SLA/SLO? What is the target, how many consecutive months/quarters have you held it, and roughly how many out-of-hours pages does on-call get per week now vs when you started?
> n/a
25. On the multi-cloud and on-prem work: any measured cost reduction — percentage of cloud spend cut, VM/server consolidation count, or licensing eliminated (VMware sockets, commercial tools replaced with open source)? Even a rough annual figure or "avoided buying N servers."
> none
26. Which compliance regimes does your platform fall under (PCI-DSS, ISO 27001, SWIFT CSP, Bank of Ghana exams, internal/external audit), and did your controls help pass an audit or close specific findings? How many findings, any under deadline?
> PCI-DSS, ISO 27001, internal/external audit. Segregation of creds, incident runbooks, change management and code review processes helped pass audits 
27. In your DR drills, what RTO/RPO did you actually hit (not just the 45-minute target), and did it improve across tests? How many full failover drills have you run, and has the bank ever had a real outage where the runbooks were used in anger — with what recovery time and impact?
> No real disaster yet. RPO=0 and RTO=22mins improve from 1hr on first run
28. After wiring Veracode and Trivy in: roughly how many vulnerabilities/critical CVEs did you start catching or blocking, do you enforce a patch SLA, what percentage of deployments pass through mandatory scanning, and did you ever block a release on a finding?
> All findings of severity exceeding medium are blocked. About 10-15 were identified per app. Patches are required before deployment or sometimes deffered in a two week window for extensive fixes. All deployments subject to scanning
29. After founding the DevOps practice, how many teams or developers across the bank adopted your Git workflows and CI/CD, and how many apps did you onboard to Kubernetes/GitOps? Any measured change in deployment frequency or lead time org-wide?
> due to bearucratic change management process deployment frequency is still hampered as each change need sign off by many stakeholders. However, system is setup to handle 1 per 5mins deployments around the clock. 10 app migrate to k8s others outdate/not container ready. migration is WIP
30. For the Basis-to-Finacle cutover: how many accounts or how much data was migrated, what was the planned downtime window and did you beat it, how many critical defects did QA catch before go-live vs leaked, and was it zero data loss?
> 3 million + accounts downtime of 3hrs. We were upp in 2. No major defects slipped a few minors 

## Theme 6 — Credentials, timeline, and positioning

31. How far into TOGAF self-study are you — booked an exam date, finished a specific course, or still reading the standard? Have you applied any TOGAF or ArchiMate concept to a real diagram or decision at work?
> no. not far we can drop togaf
32. What was the full Oracle program you went through in mid-2025 — OCI-focused, tied to the VMware/Tanzu or Finacle work — and did it come with any other modules or certificates beyond the three listed? During the Finacle-on-Tanzu work, did VMware, Infosys/Finacle, Elastic, or Red Hat run any official training that gave you a completion certificate? Does the bank require any mandatory security/compliance certification (ISO 27001, PCI-DSS, infosec) you have completed?
> not related to finacle standalone self study. No training provided and not cert requirement
33. Have you ever sat or studied for any Kubernetes (CKA/CKAD/CKS), AWS Solutions Architect Associate, HashiCorp Terraform Associate, or Azure (AZ-104/AZ-305) cert — even partially or scheduled and not sat?
> yes currently working towards CKA, CKS, AWS SAA and SAP. Previously studied for GCP architect but did not write exam. Also currently enrolled in Google Cyber security on coursera. 
34. At GTBank, did your DevOps Lead role end when you became Core Banking Services Lead, or do you hold both at once? Was core banking a formal promotion, a lateral scope expansion, or a second hat?
> second hat hold both simultaneously with scope expansion. Also responsible to for code reviews and approval for all code related changes bankwide. 
35. What were you doing between graduating in May 2020 and starting at MyHealthCop in January 2021 — national service, freelance, contract work? And was there any paid engineering work before MyHealthCop we are not counting?
> national service and freelance projects
36. Have you given any talks (meetups, conferences, internal brown-bags) or published any writing (blog posts, threads, erifoundry research)? What is actually on your public GitHub (github.com/cyteger), including any PR merged into a well-known project?
> MC/Moderator at 2025 Microsoft , owner of risingEngineers substack that publishes engineering articles
37. Did you personally hire or interview for the DevOps and QA teams? Did the DevOps team grow beyond the original 4? Have you mentored juniors who got promoted or took on bigger scope? Roughly how many engineers have reported to you or been mentored by you across all roles?
> Personaly interviewed all members of my team. Mentored juniors to go from regular devops to core banking service management. 13 engineers report to me in total accross myhealthcop and and GTBank
38. For international remote roles: have you worked day-to-day with teammates or clients in other timezones (US, EU, UK)? Want a short line stating your GMT timezone and overlap window? And which one or two titles would you actually accept — Platform Engineer, SRE, DevOps Lead, Solutions Architect, Full-Stack Engineer, or Engineering Manager?
> worked with bandana.com as freelance DevOps engineer from oct 2025 to jan 2026 in UTC -4, -5 timezone. No timezone on resume. DevOps Engineer, Solutions Architect
