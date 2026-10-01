<h1>Hi, I'm Ronan!</h1>

**AI Cybersecurity Intern @ Abbott** &middot; MS Cybersecurity @ Northeastern, Khoury College

### [ronankongala.github.io](https://ronankongala.github.io) &middot; 25 case studies with write-ups

<a href="https://www.linkedin.com/in/ronan-kongala">LinkedIn</a> &middot;
<a href="mailto:kongalaronan@gmail.com">kongalaronan@gmail.com</a> &middot;
Boston, MA

<h2>Featured Projects</h2>

_Selected work below. The complete log of 25 cases, filterable by tag, lives at [ronankongala.github.io](https://ronankongala.github.io)._

- <b>Red Team C2 Lab: Sliver C2 Adversary Emulation (CASE-26)</b>
  - Ran Sliver C2 v1.7.7 against a Windows 11 Enterprise victim on an isolated VMware NAT network, executing 7 MITRE ATT&CK techniques from HTTPS beacon delivery to exfiltration over the C2 channel
  - Dumped the SAM and SYSTEM hives, parsed 5 accounts with pypykatz, and authenticated over SMB with pass-the-hash through impacket
  - Ships with 3 Sigma detection rules, an ATT&CK Navigator layer, and a red team report
  - [GitHub Repo](https://github.com/ronankongala/red-team-c2-lab)

- <b>FraudSentry: Fraud Detection, SHAP Explainability + Fairness Audit (CASE-25)</b>
  - Compared 4 models on the IEEE-CIS dataset with a time-based split; RandomForest led at 0.748 ROC-AUC, catching 649 of 4,064 held-out fraud cases at a 3% false-positive budget
  - A fairness audit found a 23.7-point false-positive-rate spread across merchant categories, documented next to SHAP explanations and a GDPR DPIA
  - [GitHub Repo](https://github.com/ronankongala/fraudsentry)

- <b>VulnTrack: Full-Stack Vulnerability Management with a DevSecOps Pipeline (CASE-23)</b>
  - Spring Boot 4 and React vulnerability tracker on PostgreSQL with JWT authentication
  - The Jenkins pipeline's SonarQube SAST gate caught a BLOCKER and a CRITICAL violation, then passed once both were fixed
  - Deployed to Kubernetes with Helm (3 pods, 0 restarts), with Burp Suite DAST findings written up
  - [GitHub Repo](https://github.com/ronankongala/vulntrack)

- <b>Zero Trust Test Bed: mTLS, OIDC, OPA + Just-in-Time Vault Credentials (CASE-22)</b>
  - Every request to the 3 microservices clears 4 layers: mutual TLS, Keycloak OIDC, OPA policy, and Vault credentials
  - 7 of 7 Rego tests pass, and a live 403 versus 200 split depends only on token roles
  - Vault credentials expire after 20 seconds and are rejected afterward; each control maps to NIST SP 800-207
  - [GitHub Repo](https://github.com/ronankongala/zerotrust-lab)

- <b>FedRAMP RMF Compliance Lab: STIG Hardening, OpenSCAP + POA&M (CASE-21)</b>
  - Took an Ubuntu 24.04 host through a FedRAMP Moderate RMF cycle with OpenSCAP and Ansible
  - The DISA STIG V1R5 score rose from 69.58% to 78.06% after 13 Ansible changes with 0 failures
  - 7 residual findings went into a POA&M, and the SSP covers all 20 NIST 800-53 Rev 5 families
  - [GitHub Repo](https://github.com/ronankongala/fedramp-rmf-lab)

- <b>Zeek Network Forensics + Beacon Detection (CASE-17)</b>
  - Zeek 8.2.1 turned an SSLoad and Cobalt Strike PCAP into 17 structured logs
  - RITA flagged 85.239.53.219 as a beacon (score 0.504, 477 second mean interval)
  - 3 Jupyter threat hunting notebooks and 2 Sigma rules, mapped to 6 MITRE ATT&CK techniques
  - [GitHub Repo](https://github.com/ronankongala/zeek-network-forensics-lab)

- <b>Malware Analysis Lab: AgentTesla Static, Dynamic + Memory Forensics (CASE-16)</b>
  - Reverse engineered an AgentTesla stealer with PEStudio, CAPA, and Ghidra, finding MurmurHash API hashing
  - Wrote 3 YARA rules with zero false positives; the Any.run sandbox produced 87 IOCs, and its verdict also tagged Stealc/Vidar
  - Volatility 3 found code injection in SearchApp.exe and powershell.exe in a 7GB memory dump
  - [GitHub Repo](https://github.com/ronankongala/malware-analysis-lab)

- <b>AppSec Pipeline + Secrets Management Lab (CASE-15)</b>
  - Wrapped OWASP WebGoat in a 3-gate CI/CD pipeline: Semgrep SAST (66 findings across 1,002 files), Checkov (3 Dockerfile misconfigurations) and Trivy (71 CVEs in the container image)
  - An OWASP ZAP active scan (961 requests) found 8 vulnerability categories, including missing CSRF protections
  - Moved credentials into the HashiCorp Vault KV engine with a rotation demo, and set up Okta OIDC SSO with MFA through Okta Verify
  - Mapped the environment against 16 PCI-DSS 4.0 requirements with an accepted risk register
  - [GitHub Repo](https://github.com/ronankongala/Appsec-pipeline-lab)

- <b>Access-Governed RAG Console: LLM Access Control + Entra ID SSO (CASE-14)</b>
  - Role-based access control runs at the retrieval layer, so restricted documents never reach the model for a user without the role
  - Microsoft Entra ID (OAuth2) sign-in maps app-role claims to backend RBAC, with a demo-login fallback that needs no external setup
  - A prompt-injection scanner resisted 10 of 10 cases in an attack battery; every access decision is audit-logged, and the app runs on Azure App Service
  - [GitHub Repo](https://github.com/ronankongala/Access-governed-rag-console)

<h3>More projects</h3>

- **[GuardDutySync](https://github.com/ronankongala/guardduty-sync) (CASE-20):** polls AWS GuardDuty with boto3, maps 13 finding types to 12 MITRE ATT&CK techniques, and opens Jira tickets. A second run skipped all 10 tickets from the first as duplicates.
- **[Authorized Penetration Test, Metasploit Lab](https://github.com/ronankongala/metasploit-pentest-report) (CASE-19):** exploited CVE-2011-2523 (vsftpd backdoor), CVE-2007-2447 (Samba RCE) and CVE-2017-0144 (EternalBlue) on Metasploitable2 and TryHackMe Blue, then wrote up 4 findings with CVSS scores, ATT&CK mapping and remediation.
- **[Zeek Beacon Detector in OCaml](https://github.com/ronankongala/zeek-beacon-ocaml) (CASE-18):** a functional port of the CASE-17 beacon scoring that isolates 10.0.0.5 at a 477.1s mean interval and variance 1.84.
- **[NIST 800-171 / CMMC Compliance Baseline Lab](https://github.com/ronankongala/nist-cmmc-compliance-lab) (CASE-13):** Active Directory, Group Policy, Intune device compliance and Entra ID Conditional Access, with a System Security Plan. The CMMC Level 2 self-assessment scored 12 of 15 practices met, and the remaining gaps are documented as next steps.
- **[Agentic SOC Analyst](https://github.com/ronankongala/agentic-soc-sentinel) (CASE-04):** Claude queries Microsoft Sentinel through KQL, triages alerts, maps them to MITRE ATT&CK, and drafts incident summaries for human review.
- **[AWS CloudTrail Threat Detection Pipeline](https://github.com/ronankongala/aws-cloudtrail-threat-detector) (CASE-05):** CloudTrail events trigger a Lambda function that checks 11 ATT&CK-mapped rules and alerts through SNS. Email alerts fired on all 6 test invocations with no Lambda errors.
- **[Suricata IDS + ELK Stack on AWS EC2](https://github.com/ronankongala/suricata-ids-elk-lab) (CASE-06):** Suricata 7.0.3 with custom rules, shipped through Filebeat to Elasticsearch and charted in Kibana.
- **[S3 Security Auditor](https://github.com/ronankongala/s3-security-auditor) (CASE-07):** a boto3 tool that runs 6 checks per bucket (public ACL, encryption, versioning, logging and more) and writes a JSON risk report.
- **[SOC Automation Lab with AI Threat Analysis](https://github.com/ronankongala/SOC-Automation-Lab) (CASE-02):** Windows event logs flow through Splunk and n8n to OpenAI GPT-4, and the verdict posts to Slack in under 60 seconds. Tested on failed-logon events. [Event journey](https://github.com/ronankongala/SOC-Automation-Lab#implementation-flow-event-journey)
- **[SOC 2 Type I Audit Simulation](https://github.com/ronankongala/SOC2-Audit-Lab) (CASE-03):** a mock audit of that SOC automation lab against CC6, CC7 and A1, with a risk assessment, control mapping and 6 findings.
- **[Fake Job Posting Detection](https://github.com/ronankongala/Fake-Job-Posting-Detection) (CASE-01, IEEE ICAISS 2025):** ensemble ML (Random Forest, XGBoost, Gradient Boosting, AdaBoost) with SMOTE/ADASYN balancing reached 98% accuracy on 9,000+ postings. Presented at the 3rd International Conference on Augmented Intelligence and Sustainable Systems. [Read the paper](https://github.com/ronankongala/Fake-Job-Posting-Detection/blob/main/IEEE%20paper%20pdf.pdf)
- **[Kali Linux SSH MCP Bridge](https://github.com/ronankongala/kali-ssh-mcp) (CASE-12):** connects Claude Desktop to a Kali Linux terminal over SSH through the Model Context Protocol, for AI-assisted penetration testing.

<h2>Coursework</h2>

- <b>CS-5770: Software Vulnerabilities and Security</b>
  - Security challenges in network forensics, web exploitation and privilege escalation, with written methodology for packet analysis, SQL injection, command injection and Unix security
  - Tools: Wireshark, Nmap, Burp Suite
  - _Private repo (course policy). Write-ups available on request._

- <b>CY5001: Cybersecurity Technologies, Threats and Defense</b>
  - Linux security, cryptography and network defense: GPG/PGP encryption, OpenSSL operations, digital signatures and hybrid encryption
  - Wrote Bash scripts for system hardening and threat detection
  - _Private repo (course policy). Write-ups available on request._

<h2>Professional Experience</h2>

- **AI Cybersecurity Intern** at Abbott, Madison WI (Hybrid) &middot; Sep 2026 to Present
  - Contributing to ExmanIq, an internal vulnerability management platform that tracks 22,000+ vulnerabilities across organizational assets with a predictive Impact x Likelihood risk model enriched with EPSS and NVD threat intelligence
  - Diagnosed a 27-day silent data-pipeline failure after spotting an anomalous flat trend in the platform's composite risk score
  - With a teammate, built CrowdCheck Hive, which pulls CrowdStrike, Microsoft Intune and ServiceNow CMDB data together to find devices missing endpoint security coverage
  - Python, Microsoft Azure Machine Learning

- **Cybersecurity Intern** at Exact Sciences, Madison WI (Hybrid) &middot; Jun 2026 to Sep 2026
  - Automated KeyCheck, a credential-risk monitoring pipeline that scans 1,300+ application registrations for expiring credentials before they cause an incident
  - Co-built Baseline Guardian, an endpoint compliance check that compares CrowdStrike, Microsoft Intune, Tanium and ServiceNow CMDB records to assess security posture

- **Teaching Assistant, CY5001** at Northeastern University, Khoury College &middot; Jan 2026 to Apr 2026
  - Ran lab sessions and graded 200+ assignments for 61 graduate students in Cybersecurity Threats and Defenses, resolving 150+ Piazza queries within a 24-hour SLA and cutting lab completion time by 30%

- **[Cybersecurity Intern](./Cyber%20security%20NIELIT%20internship.pdf)** at NIELIT Virtual Academy, Ministry of Electronics and IT &middot; Aug 2024 to Oct 2024
  - Assessed network security across 3 live environments with Nmap and Docker, and used Random Forest models to detect anomalies in security data

- **[Web Development Trainee](./Quizaro%20web%20development%20internship.pdf)** at Quizaro ExtendedEdge (Remote) &middot; Feb 2024 to Apr 2024
  - Completed an ISO 9001:2015 certified specialization in frontend architecture and web technologies

- **[Data Science Analyst Intern](./Rejolt%20data%20science%20internship.pdf)** at Rejolt Edtech Pvt Ltd, Hyderabad &middot; Oct 2023 to Nov 2023
  - Automated data extraction pipelines for client reporting with Python (NumPy, Pandas, scikit-learn)

<h3>Industry Simulations</h3>

- **[Deloitte Cybersecurity Job Simulation](https://forage-uploads-prod.s3.amazonaws.com/completion-certificates/9PBTqmSxAf6zZTseP/E9pA6qsdbeyEkp3ti_9PBTqmSxAf6zZTseP_4yHEByFJwhmmE2ekD_1752751473837_completion_certificate.pdf)** (Forage): wrote an executive-level security report.
- **[Tata Cybersecurity Analyst Simulation](https://forage-uploads-prod.s3.amazonaws.com/completion-certificates/ifobHAoMjQs9s6bKS/gmf3ypEXBj2wvfQWC_ifobHAoMjQs9s6bKS_4yHEByFJwhmmE2ekD_1752754071792_completion_certificate.pdf)** (Forage): analyzed security logs and built an incident timeline.

<h2>Certifications and Training</h2>

- **[Google Professional Cybersecurity Certificate](https://www.coursera.org/account/accomplishments/professional-cert/NJ06LAXOT3R4)** (Completed 2025)
  - 8-course program covering security fundamentals, network security, incident response and Python automation

<details>
<summary><b>View Individual Course Certificates</b></summary>
<br>

- **Foundations of Cybersecurity**: [Certificate](https://coursera.org/verify/FNTNZKCDRVMY)
  - CIA triad, security frameworks, threat modeling
- **Risk Management**: [Certificate](https://coursera.org/verify/DT6S1IY4EMF6)
  - Risk assessments, security controls, compliance
- **Network Security**: [Certificate](https://coursera.org/verify/DKAND3ULAGT0)
  - TCP/IP, subnetting, firewall configuration, VPNs
- **Linux and SQL Security**: [Certificate](https://coursera.org/verify/8HYG23DYBTTO)
  - System hardening, database security, log analysis

**Quick References and Exercises**:
- [Linux Commands Guide](./Reference%20Guide%20Linux.pdf)
- [SQL Security Reference](./Reference%20Guide%20SQL.pdf)
- [Cybersecurity Glossary](./Google-Cybersecurity-Certificate-glossary.pdf)
- [Network Traffic Incident Report](./Cybersecurity-incident-report-network-traffic-analysis.pdf)
- [SQL Query Filtering Exercise](./Apply%20filters%20to%20SQL%20queries.pdf)
</details>

<h2>Education</h2>

- **MS Cybersecurity**, Northeastern University, Boston (2025 to 2027)
  - GPA: 3.86/4.0
  - Relevant Coursework: Software Vulnerabilities and Security (CS-5770), Cybersecurity Technologies, Threats and Defense (CY5001), Network Forensics
  - Focus: Applied cryptography, secure systems, threat analysis

- **B.Tech AI and Data Science**, Vardhaman College of Engineering (2021 to 2025)
  - Focus: Machine Learning, Data Mining, Statistical Analysis
  - Capstone: AI-based Intrusion Detection System

<h2>Technical Skills</h2>

**Network Forensics**: Zeek • RITA • Wireshark • Beacon Detection • PCAP Analysis • Jupyter • Sigma Rules  
**Malware Analysis**: PEStudio • CAPA • Ghidra • YARA • CAPE Sandbox • Any.run • winpmem • Volatility 3  
**Vulnerability Management**: Nessus • OpenSCAP • DISA STIG • EPSS • NVD • CVSS v3.0 • Risk Scoring • POA&M  
**Detection and SIEM**: Splunk • Microsoft Sentinel • KQL • Suricata • Elastic/ELK • AWS GuardDuty  
**Offensive Security**: Metasploit • Nmap • Burp Suite • Kali Linux • OWASP ZAP • Sliver C2 • impacket • pypykatz  
**AppSec and CI/CD**: Semgrep • SonarQube • Trivy • Checkov • Jenkins • GitHub Actions • Terraform • HashiCorp Vault • Okta OIDC  
**Endpoint and Asset**: CrowdStrike • Microsoft Intune • Tanium • ServiceNow CMDB  
**Identity and Compliance**: Active Directory • Group Policy • Microsoft Entra ID • Conditional Access • NIST 800-171 • CMMC • FedRAMP Moderate • SOX/COSO • GDPR (Article 35 DPIA, Articles 15/17)  
**Zero Trust and Access Control**: Keycloak (OIDC / SAML 2.0) • Open Policy Agent • Rego • mutual TLS / PKI • HashiCorp Vault just-in-time credentials • NIST SP 800-207  
**Cloud Security**: AWS CloudTrail • AWS Lambda • Amazon S3 • boto3 • GCP • Azure • Azure App Service  
**AI and Automation**: Claude AI • OpenAI GPT-4 • n8n • Model Context Protocol (MCP) • RAG • LLM Security • Prompt Injection Defense • Jira REST API  
**ML and Model Assurance**: scikit-learn • XGBoost • SHAP • imbalanced-learn (SMOTE) • Subgroup Fairness Auditing • Model Explainability  
**Cryptography**: OpenSSL • GPG/PGP • AES • RSA • Digital Signatures  
**Programming**: Python • Java (Spring Boot) • SQL • Bash • PowerShell • KQL • JavaScript • TypeScript (React) • OCaml  
**Platforms**: Linux • Windows Server • Docker • Kubernetes • Helm • PostgreSQL • VMware • AWS • Azure • GCP • Ansible  
**Frameworks**: MITRE ATT&CK • NIST SP 800-30 • NIST SP 800-207 • NIST SP 800-53 Rev 5 • NIST SP 800-171 • NIST CSF • CMMC • FedRAMP • CIS Controls • OWASP Top 10 • PCI DSS 4.0 • SOC 2  

<h2>Connect With Me</h2>
<p>
  <a href="https://www.linkedin.com/in/ronan-kongala">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="mailto:kongalaronan@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
  </a>
  <a href="https://github.com/ronankongala">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
  </a>
</p>

---
*Seeking Summer and Fall 2027 cybersecurity co-op and internship roles in SOC and detection engineering, malware analysis, cloud security, vulnerability management, GRC, and AI/LLM security.*
