<h1>Hi, I'm Ronan!</h1>

**AI Cybersecurity Intern @ Abbott** &middot; MS Cybersecurity @ Northeastern, Khoury College

### 🔗 [ronankongala.github.io](https://ronankongala.github.io) &middot; 24 case studies with full write-ups

<a href="https://www.linkedin.com/in/ronan-kongala">LinkedIn</a> &middot;
<a href="mailto:kongalaronan@gmail.com">kongalaronan@gmail.com</a> &middot;
Boston, MA

<h2>🚀 Featured Projects</h2>

_Selected work below. The full log of 24 cases, filterable by tag, lives at [ronankongala.github.io](https://ronankongala.github.io)._

- <b>FraudSentry: Fraud Detection, SHAP Explainability + Fairness Audit (CASE-25)</b>
  - Built a fraud detection pipeline on the real IEEE-CIS dataset, comparing 4 models on a time-based split
  - RandomForest led at 0.748 ROC-AUC, catching 649 of 4,064 held-out fraud cases at a 3% false-positive budget
  - Added SHAP explainability, a fairness audit that found a 23.7-point false-positive-rate spread, and a GDPR DPIA
  - [GitHub Repo](https://github.com/ronankongala/fraudsentry)

- <b>VulnTrack: Full-Stack Vulnerability Management with a DevSecOps Pipeline (CASE-23)</b>
  - Built a Spring Boot 4 and React vulnerability tracker on PostgreSQL with JWT authentication
  - Jenkins pipeline with a SonarQube SAST gate that caught a BLOCKER and a CRITICAL violation, then passed once both were fixed
  - Deployed to Kubernetes with Helm (3 pods, 0 restarts) and documented Burp Suite DAST findings
  - [GitHub Repo](https://github.com/ronankongala/vulntrack)

- <b>Zero Trust Test Bed: mTLS, OIDC, OPA + Just-in-Time Vault Credentials (CASE-22)</b>
  - Built 3 microservices where every request clears 4 layers: mutual TLS, Keycloak OIDC, OPA policy, and Vault credentials
  - 7 of 7 Rego tests passing, with a live 403 versus 200 split driven only by token roles
  - 20 second Vault credentials rejected after expiry; every control mapped to NIST SP 800-207
  - [GitHub Repo](https://github.com/ronankongala/zerotrust-lab)

- <b>FedRAMP RMF Compliance Lab: STIG Hardening, OpenSCAP + POA&M (CASE-21)</b>
  - Carried an Ubuntu 24.04 host through a full FedRAMP Moderate RMF cycle with OpenSCAP and Ansible
  - Raised the DISA STIG V1R5 score from 69.58% to 78.06% through 13 Ansible changes with 0 failures
  - Tracked 7 residual findings in a POA&M and produced an SSP across all 20 NIST 800-53 Rev 5 families
  - [GitHub Repo](https://github.com/ronankongala/fedramp-rmf-lab)

- <b>GuardDutySync: GuardDuty to MITRE ATT&CK to Jira Pipeline (CASE-20)</b>
  - Built a Python pipeline that polls AWS GuardDuty findings with boto3 and enriches them with MITRE ATT&CK data
  - Mapped 13 finding types to 12 techniques and auto-created Jira tickets through the REST API
  - Idempotent reruns: 10 tickets created on the first run, 10 duplicates skipped on the second
  - [GitHub Repo](https://github.com/ronankongala/guardduty-sync)

- <b>Authorized Penetration Test, Metasploit Lab (CASE-19)</b>
  - Ran authorized penetration tests against Metasploitable2 and TryHackMe Blue, with Nmap recon from Kali Linux
  - Exploited 3 CVEs with the Metasploit Framework: CVE-2011-2523 (vsftpd backdoor), CVE-2007-2447 (Samba RCE), and CVE-2017-0144 (EternalBlue)
  - Documented 4 findings with CVSS scoring, MITRE ATT&CK mapping, and remediation steps
  - [GitHub Repo](https://github.com/ronankongala/metasploit-pentest-report)

- <b>Zeek Beacon Detector (OCaml) (CASE-18)</b>
  - Ported the CASE-17 beacon-scoring logic to OCaml to compare imperative and functional approaches
  - Groups Zeek conn.log connections by source IP and flags low-variance periodic senders as C2 beacon candidates
  - Isolated 10.0.0.5 at a 477.1s mean interval and variance 1.84 against two high-variance talkers
  - [GitHub Repo](https://github.com/ronankongala/zeek-beacon-ocaml)

- <b>Zeek Network Forensics + Beacon Detection (CASE-17)</b>
  - Ran Zeek 8.2.1 against a real SSLoad and Cobalt Strike PCAP, generating 17 structured logs
  - RITA flagged 85.239.53.219 as a beacon (score 0.504, 477 second mean interval)
  - Built 3 Jupyter threat hunting notebooks and 2 Sigma rules, mapped to 6 MITRE ATT&CK techniques
  - [GitHub Repo](https://github.com/ronankongala/zeek-network-forensics-lab)

- <b>Malware Analysis Lab: AgentTesla Static, Dynamic + Memory Forensics</b>
  - Reverse engineered a real AgentTesla stealer with PEStudio, CAPA, and Ghidra, finding MurmurHash API hashing
  - Wrote 3 YARA rules with zero false positives and confirmed 87 IOCs in the Any.run sandbox
  - Detected code injection in SearchApp.exe and powershell.exe with Volatility 3 on a 7GB memory dump
  - [GitHub Repo](https://github.com/ronankongala/malware-analysis-lab)

- <b>AppSec Pipeline + Secrets Management Lab</b>
  - Wrapped OWASP WebGoat with a 3-gate CI/CD security pipeline: Semgrep SAST (66 findings across 1,002 files), Checkov (3 Dockerfile misconfigurations), Trivy (71 CVEs in container image)
  - OWASP ZAP active scan (961 requests) found 8 vulnerability categories including missing CSRF protections
  - Migrated credentials into HashiCorp Vault KV engine with secret rotation demo; configured Okta OIDC SSO with MFA enforcement via Okta Verify
  - Mapped full environment against 16 PCI-DSS 4.0 requirements with an accepted risk register
  - [GitHub Repo](https://github.com/ronankongala/Appsec-pipeline-lab)

- <b>Access-Governed RAG Console (LLM Access Control + Entra ID SSO)</b>
  - Built a RAG assistant that enforces role-based access control at the retrieval layer, so restricted documents are excluded from a non-authorized user's candidate set before the model ever sees them
  - Integrated real Microsoft Entra ID (OAuth2) sign-in with app-role claims mapped to backend RBAC, plus a demo-login fallback so the repo runs with zero external setup
  - Added a prompt-injection scanner (validated by a 10-case attack battery, 10/10 resisted) and full audit logging of every access decision; deployed to Azure App Service
  - [GitHub Repo](https://github.com/ronankongala/Access-governed-rag-console)

- <b>NIST 800-171 / CMMC Compliance Baseline Lab</b>
  - Configured Active Directory, Group Policy, Microsoft Intune device compliance, and Entra ID Conditional Access requiring device compliance for cloud app access
  - Hardened Windows Defender Firewall rules and authored a System Security Plan mapping every control to its NIST 800-171 requirement
  - Built a CMMC Level 2 self-assessment scorecard scoring 12 of 15 practices met, with remaining gaps documented as next steps
  - [GitHub Repo](https://github.com/ronankongala/nist-cmmc-compliance-lab)

- <b>Agentic SOC Analyst (Microsoft Sentinel + Claude AI)</b>
  - Built an agentic AI-powered SOC analyst integrating Microsoft Sentinel with Claude AI
  - Automated KQL query generation, alert triage, and MITRE ATT&CK threat mapping
  - Designed for real-world incident detection and AI-assisted response workflows
  - [GitHub Repo](https://github.com/ronankongala/agentic-soc-sentinel)

- <b>AWS CloudTrail Threat Detection Pipeline</b>
  - Engineered a serverless threat detection pipeline using CloudTrail, Lambda, SNS, and DynamoDB
  - Implemented 11 detection rules mapped to MITRE ATT&CK, covering Defense Evasion, Privilege Escalation, and Credential Access
  - Confirmed end-to-end real-time email alerting with 100% Lambda execution success rate across 6 invocations
  - [GitHub Repo](https://github.com/ronankongala/aws-cloudtrail-threat-detector)

- <b>Suricata IDS + ELK Stack on AWS EC2</b>
  - Deployed Suricata 7.0.3 IDS on AWS EC2 with custom detection rules monitoring live network traffic
  - Built a log ingestion pipeline (Suricata to Filebeat to Elasticsearch) indexing 110+ security events
  - Designed Kibana dashboards visualizing alert signatures and event type distribution
  - [GitHub Repo](https://github.com/ronankongala/suricata-ids-elk-lab)

- <b>S3 Security Auditor</b>
  - Built a Python (boto3) tool to audit AWS S3 buckets for misconfigurations
  - Performed 6 security checks per bucket covering public ACL, encryption, versioning, and logging with severity classification
  - Generated structured JSON risk reports for remediation tracking
  - [GitHub Repo](https://github.com/ronankongala/s3-security-auditor)

- <b>SOC Automation Lab with AI Threat Analysis</b>
  - Built end-to-end security pipeline: Windows to Splunk to n8n to OpenAI to Slack
  - Automated threat detection with MITRE ATT&CK mapping and AI-powered analysis
  - Achieved under 60s detection and under 9s processing time for security incidents
  - [GitHub Repo](https://github.com/ronankongala/SOC-Automation-Lab) | [View Demo](https://github.com/ronankongala/SOC-Automation-Lab#implementation-flow-event-journey)

- <b>SOC 2 Type I Audit Simulation</b>
  - Conducted a simulated SOC 2 Type I audit of a personal SOC automation lab
  - Produced formal deliverables: risk assessment, control mapping, and findings report
  - Demonstrated GRC skills including trust service criteria, evidence collection, and gap analysis
  - [GitHub Repo](https://github.com/ronankongala/SOC2-Audit-Lab)

- <b>Fake Job Posting Detection (Published Research: IEEE ICAISS 2025)</b>
  - Detected fraudulent job listings using ensemble ML (Random Forest, XGBoost, Gradient Boosting, AdaBoost)
  - Achieved 98% accuracy across 9,000+ records using SMOTE/ADASYN class balancing
  - Presented at the 3rd International Conference on Augmented Intelligence and Sustainable Systems (ICAISS 2025)
  - [Read the Paper](https://github.com/ronankongala/Fake-Job-Posting-Detection/blob/main/IEEE%20paper%20pdf.pdf) | [GitHub Repo](https://github.com/ronankongala/Fake-Job-Posting-Detection)

- <b>Kali Linux SSH MCP Bridge</b>
  - Built a Claude Desktop to Kali Linux SSH bridge via Model Context Protocol (MCP)
  - Enables AI-assisted penetration testing and security research directly from Claude Desktop
  - Bridges natural language commands to live Kali Linux terminal execution
  - [GitHub Repo](https://github.com/ronankongala/kali-ssh-mcp)

- <b>Security Analysis and Hardening Projects</b>
  - Network Security: Configured firewalls, VPNs, and IDS/IPS using Snort with Wireshark analysis
  - Web Security: Built SQL injection detection system and analyzed database security vulnerabilities
  - Linux Hardening: Automated security configurations implementing CIS benchmarks
  - [Network Security Report](./Cybersecurity-incident-report-network-traffic-analysis.pdf) | [SQL Analysis](./Apply%20filters%20to%20SQL%20queries.pdf) | [Linux Guide](./Reference%20Guide%20Linux.pdf)

<h2>📖 Coursework</h2>

- <b>CS-5770: Software Vulnerabilities and Security</b>
  - Hands-on security challenges: network forensics, web exploitation, privilege escalation
  - Documented methodologies for packet analysis, SQL injection, command injection, Unix security
  - Tools: Wireshark, Nmap, Burp Suite, SQL injection techniques, privilege escalation
  - _Private repo (course policy). Write-ups available on request._

- <b>CY5001: Cybersecurity Technologies, Threats and Defense</b>
  - Comprehensive coursework in Linux security, cryptography, and network defense
  - Implemented GPG/PGP encryption, OpenSSL operations, digital signatures, and hybrid encryption
  - Built automated security scripts for system hardening and threat detection
  - Skills: Linux administration, Bash scripting, AES/RSA encryption, digital envelopes, log analysis
  - _Private repo (course policy). Write-ups available on request._

<h2>🏆 Professional Experience</h2>

<h3>Security Engineering Co-op</h3>

- **AI Cybersecurity Intern** at Abbott, Madison WI (Hybrid) &middot; Sep 2026 to Present
  - Contributing to ExmanIq, an internal vulnerability management platform monitoring 22,000+ tracked vulnerabilities across organizational assets using a predictive Impact x Likelihood risk model enriched with EPSS and NVD threat intelligence
  - Diagnosed a 27-day silent data-pipeline failure by recognizing an anomalous flat trend in the platform's composite risk score
  - Built CrowdCheck Hive with a teammate, correlating CrowdStrike, Microsoft Intune, and ServiceNow CMDB data to identify device coverage gaps across the organization's endpoint security controls
  - Python, Microsoft Azure Machine Learning

- **Cybersecurity Intern** at Exact Sciences, Madison WI (Hybrid) &middot; Jun 2026 to Sep 2026
  - Built Baseline Guardian with a teammate, correlating data across multiple internal systems (CrowdStrike, Microsoft Intune, Tanium, ServiceNow CMDB) to assess security posture and endpoint compliance
  - Automated KeyCheck, a credential-risk monitoring pipeline scanning 1,300+ application registrations to identify expiring-credential risk before it became an incident

- **Teaching Assistant, CY5001** at Northeastern University, Khoury College &middot; Jan 2026 to Apr 2026
  - Ran lab sessions and graded 200+ assignments for 61 graduate students in Cybersecurity Threats and Defenses, resolving 150+ Piazza queries within a 24-hour SLA

<h3>Industry Simulations and Virtual Internships</h3>

- ✅ **[Deloitte Cybersecurity Simulation](https://forage-uploads-prod.s3.amazonaws.com/completion-certificates/9PBTqmSxAf6zZTseP/E9pA6qsdbeyEkp3ti_9PBTqmSxAf6zZTseP_4yHEByFJwhmmE2ekD_1752751473837_completion_certificate.pdf)**
  - Conducted vulnerability assessments and penetration testing
  - Developed security policies and incident response procedures
  - Created executive-level security reports

- ✅ **[Tata Cybersecurity Analyst Simulation](https://forage-uploads-prod.s3.amazonaws.com/completion-certificates/ifobHAoMjQs9s6bKS/gmf3ypEXBj2wvfQWC_ifobHAoMjQs9s6bKS_4yHEByFJwhmmE2ekD_1752754071792_completion_certificate.pdf)**
  - Performed threat hunting and malware analysis
  - Implemented security controls and monitoring solutions
  - Analyzed security logs and created incident timelines

<h3>Internships</h3>

- **[NIELIT Cybersecurity Internship](./Cyber%20security%20NIELIT%20internship.pdf)** (Aug 2024 to Oct 2024)
  - Monitored SOC operations and analyzed security alerts
  - Configured SIEM rules and correlation policies
  - Participated in incident response exercises

- **[Quizaro Web Development](./Quizaro%20web%20development%20internship.pdf)** (Feb 2024 to Apr 2024)
  - Developed secure web applications with input validation
  - Implemented OAuth 2.0 and session management
  - Conducted security code reviews

- **[Rejolt Data Science](./Rejolt%20data%20science%20internship.pdf)** (Oct 2023 to Nov 2023)
  - Built ML models for anomaly detection
  - Analyzed large datasets for pattern recognition
  - Created predictive analytics dashboards

<h2>📚 Certifications and Training</h2>

- **[Google Professional Cybersecurity Certificate](https://www.coursera.org/account/accomplishments/professional-cert/NJ06LAXOT3R4)** (Completed 2025)
  - 8-course comprehensive program covering security fundamentals, network security, incident response, and Python automation

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

**Quick References**:
- [Linux Commands Guide](./Reference%20Guide%20Linux.pdf)
- [SQL Security Reference](./Reference%20Guide%20SQL.pdf)
- [Cybersecurity Glossary](./Google-Cybersecurity-Certificate-glossary.pdf)
</details>

<h2>🎓 Education</h2>

- **MS Cybersecurity** (2025 to 2027) -- Northeastern University, Boston
  - GPA: 3.86/4.0
  - Relevant Coursework: Software Vulnerabilities and Security (CS-5770), Cybersecurity Technologies, Threats and Defense (CY5001), Network Forensics
  - Focus: Applied cryptography, secure systems, threat analysis

- **B.Tech AI and Data Science** (2021 to 2025) -- Vardhaman College of Engineering
  - Focus: Machine Learning, Data Mining, Statistical Analysis
  - Capstone: AI-based Intrusion Detection System

<h2>💼 Technical Skills</h2>

**Network Forensics**: Zeek • RITA • Wireshark • Beacon Detection • PCAP Analysis • Jupyter • Sigma Rules  
**Malware Analysis**: PEStudio • CAPA • Ghidra • YARA • CAPE Sandbox • Any.run • winpmem • Volatility 3  
**Vulnerability Management**: Nessus • OpenSCAP • DISA STIG • EPSS • NVD • CVSS v3.0 • Risk Scoring • POA&M  
**Detection and SIEM**: Splunk • Microsoft Sentinel • KQL • Suricata • Elastic/ELK • AWS GuardDuty  
**Offensive Security**: Metasploit • Nmap • Burp Suite • Kali Linux • OWASP ZAP  
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

<h2>📫 Connect With Me</h2>
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
*Currently seeking Summer/Fall 2027 cybersecurity co-op/internship opportunities in Security Operations, Incident Response, Malware Analysis, Detection Engineering, Network Forensics, or AI/LLM Security*
