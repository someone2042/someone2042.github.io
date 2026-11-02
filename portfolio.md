# Master Career & Portfolio Reference Document

## 1. Personal & Professional Identity

* **Full Name:** Mohamed El Mahdaoui


* **Current Status:** 5th-Year State Engineering Student (Ingénieur d'État — S5) in IT Security & Artificial Intelligence, seeking a 6-month End-of-Studies Internship (Stage PFE — S6).


* **Location:** Marrakech / Casablanca / Rabat, Morocco


* **Email:** mehdaoui200309@gmail.com


* **Phone:** +212 6 42 71 42 14


* **LinkedIn:** `[linkedin.com/in/mohamed-el-mahdaoui-3434b7246/](https://linkedin.com/in/mohamed-el-mahdaoui-3434b7246/)`

* **GitHub:** `[github.com/someone2042](https://github.com/someone2042)`

* **Languages:** Arabic (Native), French (Fluent), English (Technical/Fluent), German (Basic).



---

## 2. Education & Academic Curriculum

### Diplôme d'Ingénieur d'État en Sécurité Informatique (IT Security)

**Université Cadi Ayyad (UCA) — Faculté des Sciences et Techniques (FST), Marrakech** | *Sept 2024 – June 2027 (Currently in 5th Year / S5)*

* **IT Security Governance & Risk Management** 


* **Application & Service Security:** DevSecOps lifecycles, Secure SDLC, OWASP Top 10 web/API security, secure microservices, authentication/authorization architectures (OAuth 2.0, OIDC, SAML, JWT).


* **Cyber Incident Management & Digital Forensics:** Incident response lifecycles (NIST/SANS), host and memory forensics, disk artifact analysis, timeline reconstruction, and chain of custody.


* **Cloud & Blockchain Security:** Public cloud security posture (AWS/Azure IAM, VPC segmentation, KMS/Secrets Manager, logging), container security, cryptographic ledgers.


* **Banking Payment Systems & Industrial IS (OT/ICS) Security** 


* **Business Simulation, Innovation & Employment Skills:** Corporate strategy simulation, enterprise management, and professional communication.


* **Security Testing & Ethical Hacking:** Penetration testing methodologies, vulnerability assessment, web and network exploitation, post-exploitation, and reporting.


* **Network & Systems Security:** Firewalling (NGFW, iptables, pfSense), IDS/IPS (Suricata, Snort), VPNs (IPsec, TLS), network access control (802.1X/RADIUS), and OS hardening.


* **Virtualization & Cloud Computing:** Type-1/Type-2 hypervisors (VirtualBox, VMware, KVM), containerization (Docker, Docker Compose), IaaS/PaaS/SaaS architectures (AWS, Azure).


* **Software Engineering & DevOps:** CI/CD pipelines (Git, GitHub, GitLab CI/CD), automated testing, infrastructure automation, and DevSecOps integration.


* **IT Project Management, Agile & Business Management:** Agile frameworks (Scrum, Kanban), Jira backlog management, cost-benefit analysis (ACB), accounting, and enterprise finance.


* **Cryptography:** Symmetric and asymmetric encryption (AES, RSA, ECC), Diffie-Hellman key exchange (DH, ECDH, X3DH), cryptographic hash functions, HMAC, Key Derivation Functions (KDF), PKI, digital signatures, and E2EE protocols.


* **Java Programming & Security:** Secure object-oriented architecture, JVM security, memory safety, and cryptographic APIs in Java.


* **Mobile Programming & Front-End Web Dev:** Mobile application development,  modern reactive front-end frameworks (React, JavaScript/TypeScript).


* **UML Modeling & AI/IoT Power Skills:** Enterprise system modeling (Use Case, Context, Sequence, Class, and Architecture diagrams) and IoT/AI fundamentals.


* **Fundamentals of IT Security & Cyberlaw:** Core CIA triad principles, threat modeling, and comparative legal frameworks including 

* **Moroccan Law 05-20** (Cybersecurity), **Moroccan Law 09-08** (Protection of Individuals regarding Processing of Personal Data / CNDP), **French Cyberlaw** (LPM, Loi Informatique et Libertés), and **EU GDPR (RGPD)**.


* **Systems & Network Administration:** Complete Cisco CCNA curriculum (OSI/TCP-IP, VLANs, trunking, STP, OSPF, static/dynamic routing, NAT/PAT, ACLs, DHCP, DNS), Linux system administration, and Windows Server Active Directory administration.


* **Databases & Back-End Development:** Relational database design, **Oracle DBA**, **PL/SQL** programming, SQL optimization, Java OOP, PHP, Laravel, and Node.js back-end engineering.



### Licence en Mathématiques et Informatique (B.Sc. in Mathematics & Computer Science)

**Université Hassan II, Casablanca** | *Sept 2021 – June 2024*

* **Core Focus:** Advanced mathematics (linear algebra, probability, statistics, discrete math), algorithms and data structures, **C/C++** systems programming, **8086 Assembly** language, **compiler design (compilation)**, operating systems internals, computer networks, and web/database development.



---

## 3. Professional Experience (Internships)

### 1. Security Engineering Intern — Orange Cyberdefense (OCD)

**Casablanca, Morocco (On-site)** | *July 2026 – Sept 2026 (3 Months)*

During this internship, two major enterprise R&D and architecture initiatives were designed, implemented, and validated against Orange Cyberdefense operational standards:

**Project 1: Autonomous SOC Platform & System Behavior Analytics (SBA) Engine**

* **Enterprise Lab & Telemetry Engineering:** Architected a multi-subnet virtualized enterprise environment segmented via **pfSense CE (v2.8.1)** across WAN, internal LAN (`192.168.1.0/24`), and an out-of-band OPT1 management network (`192.168.56.0/24`) using Hybrid Outbound NAT and deterministic DNAT port forwarding.


* **Network & Endpoint Instrumentation:** Deployed inline **Suricata NIDS** on pfSense with the Emerging Threats (ET) ruleset and full EVE JSON output (capturing TLS SNI handshakes, HTTP metadata, DNS queries, and packet payloads), routed lossless via **syslog-ng** (`flags(no-parse)`) over UDP/514 to an Ubuntu **Wazuh SIEM Manager (v4.x)** and **OpenSearch Indexer**. Instrumented a **Windows Server 2019 Datacenter** endpoint using **Microsoft Sysmon v13** (Event IDs 1, 3, 11, 13) and Windows Security auditing (Event IDs 4624, 4672, 16384).


* **Dual-Pipeline Filebeat Ingestion:** Configured **Filebeat** to split telemetry into `wazuh-alerts-*` (for live SIEM alerting $\ge$ level 3) and `wazuh-archives-*` (`logall_json` enabled to capture 100% of raw benign and malicious system events for ML baseline training).


* **Cognitive AI Investigation Engine ("Lucid SOC"):** Built an asynchronous event-driven SOAR/triage backend using **Python**, **FastAPI**, **Asyncio**, and **SQLite** (`soc_data.db`) with automated crash recovery. Implemented a **LangGraph ReAct (Reasoning + Acting)** agent powered by **Google Gemini 3.1 Flash Lite** (`ChatGoogleGenerativeAI`) that autonomously investigates alerts with full **Glass-Box Transparency** (serializing *Thoughts*, *Actions*, and *Observations* for human auditability).


* **Deterministic Noise Filtering & Custom Agent Tools:** Engineered pre-LLM triage filters (`is_benign`) to suppress loopback and low-severity noise, optimizing token consumption. Equipped the agent with modular `@tool` integrations:


* *Dynamic SIEM Querying:* Autonomous generation of **OpenSearch DSL** queries via `AsyncOpenSearch` with built-in token context protection.


* *Threat Intelligence & Caching:* Automated IoC enrichment via **VirusTotal** (MD5/SHA256 hashes) and **AbuseIPDB** (IP reputation) backed by a 24-hour TTL SQLite cache (`soc_cache.db`) to prevent API rate-limiting.


* *Automated Active Containment:* Direct integration with the **Wazuh Manager REST API** (JWT authentication on port 55000) to trigger automated endpoint isolation (`ISOLATE_HOST`) upon high-confidence true positives.




* **Unsupervised ML System Behavior Analytics (SBA) Microservice:** Containerized (`Docker Compose`, `python:3.10-slim`) a continuous 5-minute inference daemon with zero-downtime model hot-reloading:


* *Log Parsing & Vectorization:* Applied **Drain3** streaming template mining to mask dynamic variables (IPs, GUIDs, paths) into semantic log clusters, aggregating host activity into 5-minute sliding window frequency vectors $x_t \in \mathbb{R}^m$.


* *Anomaly Detection & Calibration:* Trained an unsupervised **PyOD Isolation Forest (`IForest`)** model enhanced with synthetic outlier injection (to penalize unseen zero-day log templates) and calibrated raw decision scores via an **Empirical Cumulative Distribution Function (ECDF)** into an intuitive 0–100 percentile risk score.


* *Explainable AI (XAI) & Human-in-the-Loop Feedback:* Integrated **SHAP (`TreeExplainer`)** to compute exact marginal feature attributions ($\phi_i$) for any score $>75$, translating mathematical anomalies back into human-readable Drain3 log templates. Engineered a closed-loop *"Mark as Normal"* UI feedback system that duplicates verified benign feature vectors 50x during scheduled retraining (`train.py`) to mathematically shift tree partitioning and eliminate recurring false positives.




* **Operational Validation:** Validated end-to-end against Tier-3 SOC analyst workflows at Orange Cyberdefense using live **Lumma Stealer** malware execution (correlating Suricata TLS SNI `p3ar11fter.sbs` alerts with Sysmon Event ID 3 network sockets to PID 2644 and executing automated host isolation in 4 seconds) and complex false-positive resolution (verifying legitimate Windows `cleanmgr.exe /autoclean` DLL drops spawned by `svchost.exe` Task Scheduler).



**Project 2: Enterprise Network Security Modernization with SASE & Zero Trust Architecture**

* **Architectural Assessment:** Conducted a comprehensive technical comparative study between legacy perimeter-based architectures (hardware NGFWs, MPLS backhauling/tromboning, implicit VPN network-level trust, lateral movement exposure) and cloud-native **Gartner SASE** and **Zero Trust Architecture (ZTA)** models.


* **Zscaler Zero Trust Exchange (ZTE) Deep Dive:** Modeled enterprise deployment blueprints covering Identity & Posture (**SAML 2.0/OIDC**, **SCIM** provisioning, **Zscaler Client Connector ZCC**, **Z-Tunnel 2.0**), **Zscaler Private Access (ZPA)** with outbound-only App Connectors and micro-segmentation, **Zscaler Internet Access (ZIA)** (SWG, Layer 7 FWaaS), Inline/API **CASB**, **DLP** (Exact Data Match EDM, Indexed Document Match IDM), **SSL/TLS MITM inspection** (Single-Scan Multi-Action architecture), and unmanaged **BYOD** security via Agentless Browser Access, **Privileged Remote Access (PRA)**, and **Cloud Browser Isolation (CBI)**.


* **Cloudflare Zero Trust & AWS Proof of Concept (PoC):** Engineered a live SASE/ZTNA implementation protecting cloud infrastructure (`someonelab.site`):


* Deployed an **AWS EC2 (`t3.small`)** Ubuntu 26.04 LTS web server in `us-east-1a` with **0 inbound rules** in its AWS Security Group (completely closing ports 80 and 22 to neutralize public reconnaissance).


* Established an outbound-only **Cloudflare Tunnel (`cloudflared` / `AWS-VPC-Tunnel`)** to broker application and administrative access.


* Integrated **Microsoft Entra ID** as the centralized Identity Provider (IdP) and configured **Cloudflare One Client (WARP)** endpoint posture checks (enforcing Windows 10+ OS version, active OS firewall, and WARP gateway connectivity).


* Deployed **Browser-Rendered SSH** (`ssh.someonelab.site`) for agentless terminal administration, **SWG DNS/Network filtering policies** (blocking unauthorized categories such as gaming/Steam with custom block pages), and **SaaS API CASB integration** with **GitHub** to automatically audit repository security posture (detecting missing default branch protection and inactive repositories).





---

### 2. SOC Analyst Intern — Casanet SA (Subsidiary of Maroc Telecom)

**Rabat, Morocco (On-site)** | *July 2025 – Aug 2025 (2 Months)*

* **Behavioral Detection & Event Correlation:** Researched and applied security event correlation rules and behavioral detection methodologies within a simulated enterprise SOC environment.


* **Incident Simulation & Digital Forensics (DFIR):** Conducted simulated cyberattack scenarios to practice incident triage, digital forensics investigation, and multi-source log analysis across perimeter firewalls, IDS/IPS sensors, and Windows Event channels.



---

### 3. Full-Stack Developer Intern (AppSec Focus) — webagency-maroc

**Casablanca, Morocco (On-site)** | *July 2024 – Aug 2024 (2 Months)*

* **Centralized Administration Platform:** Designed, developed, and deployed a full-stack web administration platform used to manage all of the agency's client websites.


* **Security by Design (AppSec):** Implemented defensive coding practices aligned with the **OWASP Top 10** to prevent injection flaws, broken access control, and XSS vulnerabilities.


* **Linux Server Hardening:** Deployed production applications onto Linux servers, performing OS hardening, secure web server configuration, and granular access control management.



---

## 4. Competitions, CTFs & Hackathons

* **1st Place Winner (Premier Prix IT) — SKILL'UP 2026 Engineering Challenge (8th Edition):** EMAN Aerospace x Université Cadi Ayyad (May 18–23, 2026). Awarded the Attestation d'Excellence for architecting the winning enterprise cybersecurity solution in a multi-disciplinary Agile Kanban engineering competition.


* **Local & National CTF Competitions:** DGSSI national CTF, CGDST CTF (local in marrakech)
* **Online CTFs & Platforms:** TryHackMe (THM), PicoCTF 
* **AI & LLM Security / Jailbreaking Challenges:** Gandalf Challenge, HackTheAgent...

---

## 5. Comprehensive Project Portfolio

### Project 1: Enterprise Vulnerability & Configuration Compliance Architecture (Competition 1st Place Winner) (not that big of a deal just take the stuff to help the resume etc)

* **Official Title:** *Modèles de Solution (MDS) — Solution de Détection de Vulnérabilités et de Non-Conformités des Configurations dans un Écosystème Universitaire (Project EMAN-UCA-2026-VMDR)*.


* **Context & Problem Statement:** Conducted conception and market study to address the urgent modernization of Université Cadi Ayyad's security posture by proposing the decommissioning of a legacy **Rapid7 (Nexpose/InsightVM)** deployment—which lacked continuous configuration compliance and failed to integrate with **ServiceNow**—and modeling the architecture of a unified **Qualys VMDR** solution across on-premise, hybrid, and **Microsoft Azure** cloud environments.


* **Key Deliverables & Architectural Design:**

* **Enterprise Architecture Patterns & Modeling:** Designed formal Context Views and integration matrices applying standardized architecture patterns: `PAT.A.046` (HTTPS/TLS 1.3 telemetry transfer), `PAT.A.060` (SSO & automated provisioning), `PAT.A.066` (step-up MFA authentication for SOC analysts), `PAT.A.069` (PaaS-to-On-Prem patch deployment), `PAT.A.074` (SAML/OIDC identity federation via Auth0/Azure AD), `PAT.A.080` (active network scanner views), `PAT.A.083` (OAuth 2.0 REST API integration with ServiceNow), and `PAT.A.125` (Azure Cloud API inventory connector).

* **Financial Study & Resilience Planning:** Engineered a 5-year financial Cost-Benefit Analysis (ACB) and modeled strict endpoint resource caps, low-bandwidth scanner windows, a **4-hour RTO**, and **24-hour RPO** using local **Hybrid Collector** caching.





### Project 2: Vulnerability Discovery & Responsible Disclosure — Rosetta Stone Platform

* **Role:** Independent Security Researcher


* **Target & Vulnerability Type:** Discovered an **Insecure Answer Validation / Client-Side Validation Bypass (CWE-602)** vulnerability in the **Rosetta Stone Fluency Builder** language learning platform (React front-end communicating with `[https://gaia-server.rosettastone.com/graphql](https://gaia-server.rosettastone.com/graphql)`) used by international and Moroccan universities.


* **Technical Exploitation & Automation:**
* Identified that the React application computed exercise correctness locally in JavaScript and transmitted unverified `score` (Float), `skip`/`skipped` (Boolean), and `correct` (Boolean) parameters inside GraphQL POST mutations.


* Used **Burp Suite Community Edition** to intercept GraphQL requests and overwrite `"score":0` to `"score":1.0` and `"skip":true` to `"skip":false`, forcing backend database resynchronization to mark unanswered or failed modules as 100% completed.


* Engineered real-time, zero-touch exploitation rules using **Burp Suite Match and Replace** with regular expressions (`"score":\d+(\.\d+)?` $\rightarrow$ `"score":1`) to automatically manipulate HTTP request bodies in transit.


* Authored a formal 9-page Vulnerability Disclosure Report detailing the PoC, academic/resource allocation impact, and server-side validation remediation strategies.





### Project 3: Engineering a "Dirty" Active Directory Detection & Purple Team Lab

* **Architecture & Segmentation:** Designed and deployed a multi-zone virtualized homelab on **VirtualBox** governed by a **pfSense** router/firewall segmenting a **WAN/NAT** uplink, a **DMZ subnet (`172.16.10.0/24`)** hosting an exposed Web/DB server, and an internal **LAN/GREEN subnet (`192.168.10.0/24`)**.


* **Vulnerable Enterprise Active Directory Simulation:** Deployed a **Windows Server Active Directory Domain Controller (`192.168.10.10`)** and **Windows 10 workstation (`192.168.10.20`)**, utilizing the **BadBlood** automation tool to populate the domain with thousands of users, groups, OUs, and realistic ACL/GPO permission misconfigurations.


* **Multi-Layered Defensive Stack & Attack Simulation:** Deployed **Suricata NIDS** and **Zeek** (via network SPAN/TAP) on the perimeter, alongside **Microsoft Sysmon** and **CrowdSec** agents on Windows endpoints, forwarding all logs and threat intel syncs to a central **Wazuh SIEM (`192.168.10.50`)** and **CrowdSec Web Console**. Executed adversary emulation playbooks using **Atomic Red Team** to engineer and tune detection rules.



### Project 4: AWS Cloud Security & Automated Secret Access Monitoring Pipeline

* **Cloud Architecture:** Built an event-driven cloud security monitoring pipeline on **Amazon Web Services (AWS)** to detect unauthorized retrieval or manipulation of production credentials.


* **Workflow Implementation:** Configured **AWS Secrets Manager** to log all API activity via **AWS CloudTrail**, archiving immutable audit trails into a hardened **Amazon S3 bucket** while simultaneously streaming events to **Amazon CloudWatch Log Groups**. Engineered custom **CloudWatch Metric Filters** and **Alarms** to trigger real-time **Amazon SNS (Simple Notification Service)** email alerts to security administrators upon anomalous secret access.



### Project 5: Home Lab IoT Red Teaming & Android Smart TV Exploitation

* **Offensive Assessment:** Conducted a red team assessment against an Android Smart TV within a home lab network to evaluate the blast radius of compromised IoT appliances.


* **Exploitation & Post-Exploitation Chain:** Exploited an exposed **Android Debug Bridge (ADB — TCP port 5555)** over a flat network to gain persistent **full root shell access** (`uid=0(root)`).


* *Network Pivoting:* Utilized the compromised TV as an internal LAN jump box to scan (`ip neigh`) and target adjacent trusted devices behind the router firewall.


* *Credential & Session Theft:* Extracted cleartext Wi-Fi pre-shared keys (`PreSharedKey`) and queried local SQLite databases (`/data/data/com.google.android.gms/databases/`) to harvest active session tokens for Google and Netflix, demonstrating **2FA bypass** and account hijacking.


* *Hardware Surveillance & Persistence:* Demonstrated how tapping into the **Hardware Abstraction Layer (HAL)** enables silent microphone activation and deployed a custom **Remote Access Trojan (RAT)** APK for UI control during standby mode. Published a technical awareness breakdown detailing remediation via **Guest VLAN segmentation**, disabling UPnP, and turning off ADB developer options.





### Project 6: Cryptographic Analysis & Implementation of the Signal E2EE Protocol

* **Academic & Technical Scope:** Conducted an in-depth mathematical analysis and implementation study of the open-source **Signal Protocol** (used in Signal, WhatsApp, and Facebook Messenger) at FST Marrakech.


* **Cryptographic Mechanics Modeled:**
* **Extended Triple Diffie-Hellman (X3DH):** Modeled asynchronous session initialization using Identity Keys ($A, B$), Signed Prekeys ($U, V$), Ephemeral Keys ($Z$), and One-Time Prekeys ($T_1$), deriving a 256-bit shared Root Key via four Elliptic Curve Diffie-Hellman (ECDH) operations: $\text{root}_0 = \text{KDF}(aV, zB, zV, zT_1)$.


* **Double Ratchet Algorithm:** Modeled the interplay between the **Symmetric-key KDF Ratchet** (advancing Sending and Receiving chains $sk, rk$ to derive ephemeral message keys $msk, mrk$ that are immediately deleted after use to guarantee **Forward Secrecy**) and the **Diffie-Hellman Ratchet** (injecting new ephemeral ECDH shared secrets $DH_{ij} = \text{ECDH}(X_i, Y_j)$ into the Root Key chain on every message round-trip to guarantee **Post-Compromise / Future Secrecy**).


* **Authenticated Encryption (AE):** Formulated message encryption construction combining **AES-256-CBC** (128-bit IV) and **HMAC-SHA256**: $AE_k(T, M) = (T, \text{AES-CBC}_{IV, k_1}(M), \text{HMAC}_{k_2}(T, \text{AES-CBC}_{IV, k_1}(M)))$.





### Project 7: Comparative Cyberlaw & Data Protection Research (Morocco, France, EU)

* **Legal & Compliance Research:** Authored a comparative regulatory analysis examining the intersection of **Moroccan Law 05-20** (national cybersecurity governance, critical infrastructure operator obligations, ANSSI/DGSSI reporting), **Moroccan Law 09-08** (personal data protection regulated by the CNDP), **French Cyberlaw** (Loi Informatique et Libertés, LPM), and the **European Union GDPR (RGPD)**, mapping technical compliance controls (encryption, data retention, breach notification SLAs, DLP) to legal mandates.

### Project 8: Software, Web, Mobile, Database & Systems Engineering Portfolio

* **Full-Stack & Mobile Applications:** Engineered multiple web and mobile applications utilizing **Laravel (PHP)**, **Node.js**, **React**, **Java**, and mobile development frameworks.


* **Database Administration & Programming:** Designed relational schemas, administered **Oracle Database (DBA)** instances, and wrote stored procedures, triggers, and packages in **PL/SQL**.


* **Low-Level Systems & Compilation:** Built academic projects in **C/C++**, **8086 Assembly**, and **Compiler Design** (lexical analysis, parsing, semantic validation, and code generation).


* **AI/ML & Workflow Automation Projects:** Developed standalone Machine Learning, Deep Learning, and AI workflow automation projects in Python.


### Project 9: AI-Augmented DevSecOps Pipeline & Secure Payment Architecture

* **Academic Context:** "Sécurité des applications et des services" Module — Cycle ingénieur SIT 3 (2026/2027), Université Cadi Ayyad (FST Marrakech).


* **Architecture & Core Scope:** Engineered a comprehensive, cloud-deployable architecture encompassing a Web front-end, a Mobile application, REST/GraphQL APIs, and a back-end business logic layer.


* **DevSecOps Implementation:**
* Designed and implemented an AI-augmented DevSecOps pipeline tailored for cloud environments.


* Successfully integrated and automated all 11 Tier 1 DevSecOps security practices (based on the Prates & Pereira framework) into the CI/CD lifecycle.


* Evaluated and incorporated advanced Tier 2 DevSecOps practices to further enhance pipeline resilience.


* Deployed automated SAST, DAST, SCA, and Secret Scanning to rigorously audit both human-written code and AI-generated contributions before integration.




* **Secure Payment & Financial Risk Mitigation:**
* Developed and secured a simulated bank card payment system using a sandbox environment.


* Engineered architectural countermeasures against critical financial risks, specifically preventing transaction manipulation, unauthorized amount or beneficiary modifications, transaction replay attacks, session/token theft, account compromise, and sensitive data exposure.




* **Threat Modeling & Vulnerability Management:**
* Conducted systematic threat modeling and mitigated vulnerabilities aligned strictly with the OWASP Top 10 (2025) for Web, the OWASP Mobile Top 10, and the OWASP API Security Top 10.


* Secured AI/LLM components and development tools by applying the OWASP Top 10 for Large Language Model Applications.




* **Technical Deliverables:** Produced production-ready artifacts including full CI/CD pipeline configurations, Infrastructure as Code (IaC) files, Cloud deployment scripts, comprehensive Threat Models, and automated security scanning reports.




### Project 9 web dev project
UniCollab : une application Web qui centralise la communication, l'organisation des
tâches et le suivi de l'avancement des projets pour vos équipes.
• Création et organisation de tâches.
• Assistant IA pour des tâches plus efficaces et une meilleure productivité.
• Système de contrôle de version simple pour les fichiers de code.
• Collaboration simplifiée et communication fluide avec messagerie en temps réel.

---

## 6. Master Technical Skills & Tooling Matrix

| Category | Technologies, Frameworks & Competencies |
| --- | --- |
| **SIEM, EDR, NIDS & SecOps** | **Wazuh** (Manager, Agents, REST API, Custom Decoders/Rules, Active Response), **OpenSearch** (Indexer, DSL Queries, Dashboards), **Filebeat**, **Splunk**, **FortiSIEM**, **Suricata NIDS** (EVE JSON, DPI, Emerging Threats), **Zeek**, **CrowdSec**, **Microsoft Sysmon (v13)**, **syslog-ng**, Windows Event Logs, Threat Intelligence (**VirusTotal API**, **AbuseIPDB API**)

 |
| **SASE, Zero Trust & Network Security** | **Cloudflare Zero Trust** (Access/ZTNA, `cloudflared` Tunnels, WARP Client, Gateway SWG, DNS/L7 Firewall, CASB, Browser Isolation, Browser SSH), **Zscaler Zero Trust Exchange** (ZIA, ZPA, ZCC, Z-Tunnel 2.0, App Connectors, Inline/API CASB, DLP EDM/IDM, SSL Inspection, PRA, CBI), **Fortinet** (FortiGate NGFW, FortiSIEM), **pfSense CE** (VLANs, Hybrid Outbound NAT, DNAT, Filtering), **Cisco** (CCNA Routing & Switching, OSPF, STP, ACLs, VPN IPsec), **iptables**, RADIUS / 802.1X

 |
| **Vulnerability Mgmt, IAM & ITSM** | **Qualys Cloud Platform** , **Microsoft Entra ID (Azure AD)**, **Auth0**, SAML 2.0, OIDC, OAuth 2.0, SCIM, MFA, RBAC

 |
| **AI, Machine Learning & SecOps Automation** | **LangGraph**, **LangChain**, **Google Gemini API** (`ChatGoogleGenerativeAI`), **ReAct Cognitive Agents**, **PyOD** (Isolation Forest / `IForest`), **SHAP** (Explainable AI / `TreeExplainer`), **Drain3** (Streaming Log Template Mining), **Scikit-learn**, ECDF Calibration, Machine Learning (ML), Deep Learning (DL), AI Workflow Automation, **FastAPI**, **Asyncio**, **SQLite**<br> |
| **Cloud, Virtualization & DevSecOps** | **AWS** (EC2, VPC, Security Groups, Secrets Manager, CloudTrail, CloudWatch, S3, SNS, IAM), **Microsoft Azure**, **Docker**, **Docker Compose**, **Git**, **GitHub**, **GitLab CI/CD**, **VirtualBox**, VMware, Linux Administration & Hardening (Ubuntu/Debian), **Windows Server (2019/AD)**, Active Directory, GPO

 |
| **Offensive Security, AppSec & Crypto** | Web & API Penetration Testing (**OWASP Top 10**, GraphQL exploitation), **Burp Suite** (Proxy, Repeater, Match & Replace Regex Automation), **Nmap**, **Metasploit**, **Atomic Red Team**, **BadBlood** (AD simulation), Android/IoT Red Teaming (ADB exploitation, HAL, RATs, token extraction), **AI/LLM Security** (Prompt Injection, Filter Evasion), **Cryptography** (AES-CBC, RSA, ECC, ECDH, X3DH, Double Ratchet, KDF, HMAC, TLS 1.3 / mTLS)

 |
| **Programming, Web, Mobile & Databases** | **Python**, **Java** (OOP & Security), **C / C++**, **8086 Assembly**, Compiler Design, **Bash / Shell Scripting**, **PHP**, **Laravel**, **JavaScript**, **Node.js**, **React**, Mobile Development, **Oracle Database (DBA)**, **PL/SQL**, **SQL**, HTML5/CSS3

 |
| **Governance, Risk, Compliance (GRC) & OT** |  **NIST**,  ISO 27001/27005, **PCI-DSS**, **HIPAA**, **GDPR (RGPD)**, **Moroccan Law 05-20** (Cybersecurity), **Moroccan Law 09-08** (CNDP), French Cyberlaw, **OT/ICS/SCADA Security** (OPSWAT CIP, Industrial SI), Banking Payment Security, **UML** & **ArchiMate / Bizzdesign**, **Agile (Scrum, Kanban)**, **Jira**, Cost-Benefit Analysis (ACB), Accounting & Business Management

 |

---

## 7. Certifications & Licenses

1. **CompTIA Security+ ce Certification** — *CompTIA* (Issued Dec 2025 – Expires Dec 2028)


* *Validated Skills:* Enterprise threat mitigation, cryptography, identity and access management (IAM), zero trust architecture, enterprise SOC operations, incident response, and governance/risk/compliance (GRC).


2. **OPSWAT OT Security Expert (OTSE)** — *OPSWAT Academy* (Issued Aug 2025 | Credential ID: `a9YzoMI3AQ`)


* *Validated Skills:* Operational Technology (OT) & Industrial Control Systems (ICS) security, IT/OT network segmentation (Purdue Model), industrial malware prevention, cross-domain security, and transient device sanitization.


3. **OPSWAT Introduction to Critical Infrastructure Protection (ICIP)** — *OPSWAT Academy* (Issued Aug 2025)


* *Validated Skills:* Critical infrastructure security fundamentals, MetaDefender / Deep CDR concepts, and industrial compliance standards.


4. **Fortinet Certified Associate (FCA) in Cybersecurity** — *Fortinet* (Issued Mar 2025)


* *Validated Skills:* **FortiGate NGFW** operation, firewall policies, NAT, authentication, SSL VPN / IPsec VPN configuration, web filtering, and application control.


5. **Fortinet Certified Fundamentals (FCF) in Cybersecurity** — *Fortinet* (Issued Mar 2025)


* *Validated Skills:* Threat landscape analysis and core network security operations.


6. **Cisco Ethical Hacker** — *Cisco Networking Academy* (Issued Feb 2025)


* *Validated Skills:* Reconnaissance, vulnerability scanning, exploitation (web, network, wireless), post-exploitation, social engineering, and pentest reporting.


7. **Cisco Introduction to Cybersecurity** — *Cisco Networking Academy* (Issued Mar 2025)


8. **Cisco Networking Basics** — *Cisco Networking Academy* (Issued Nov 2023)


9. **Cisco Certified Network Associate (CCNA)** — *In Preparation (Full academic curriculum completed)*


