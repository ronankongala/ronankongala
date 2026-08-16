<h1>Hi, I'm Ronan! <br/>
  <a href="https://github.com/ronankongala">Cybersecurity Professional</a>, 
  <a href="https://www.linkedin.com/in/ronan-kongala">MS Student @ Northeastern</a>
</h1>

<h2>🚀 Featured Projects</h2>

- <b>Zeek Network Forensics + Beacon Detection (CASE-18)</b>
  - Ran Zeek 8.2.1 against a real SSLoad + Cobalt Strike PCAP (6.4MB, MTA 2024-04-18), generating 17 structured logs including conn.log, dns.log, ssl.log, kerberos.log, and ldap.log
  - Imported Zeek logs into RITA v5.1.2; scored all external connections for beacon regularity -- 85.239.53.219 flagged with rare_signature:SSLoad/1.1, beacon score 0.504, mean interval 477 seconds across 11 connections
  - Built 3 Jupyter threat hunting notebooks: conn.log duration analysis, DNS query profiling, and beacon interval visualization confirming C2 sleep timer pattern
  - Mapped findings to 6 MITRE ATT&CK techniques (T1071, T1071.004, T1008, T1095, T1557, T1018); produced IOC table and 2 Sigma detection rules in a full investigation report PDF
  - [GitHub Repo](https://github.com/ronankongala/zeek-network-forensics-lab)

- <b>Malware Analysis Lab: AgentTesla Static, Dynamic + Memory Forensics</b>
  - Reverse engineered a real AgentTesla credential stealer using PEStudio, CAPA, and Ghidra 12.1.2; identified MurmurHash API hashing at FUN_1400015a0, XOR-encrypted strings (x16), and a fraudulent DigiCert certificate chain
  - Wrote 3 custom YARA rules from extracted indicators (imphash, MurmurHash seed bytes, structural heuristics) validated with YARA 4.5.5; zero false positives across System32
  - Detonated the sample in Any.run sandbox; confirmed Stealc/Vidar stealer behavior, 32 dropped files targeting Chrome/Edge credential stores, 87 IOCs, 11 MITRE ATT&CK techniques mapped
  - Acquired live memory from FlareVM with winpmem v4.0-rc1 (7GB dump), analyzed with Volatility 3; detected PAGE_EXECUTE_READWRITE code injection in SearchApp.exe and powershell.exe
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
  - [GitHub Repo](https://github.com/ronankongala/-aws-cloudtrail-threat-detector)

- <b>Suricata IDS + ELK Stack on AWS EC2</b>
  - Deployed Suricata 7.0.3 IDS on AWS EC2 with custom detection rules monitoring live network traffic
  - Built a log ingestion pipeline (Suricata to Filebeat to Elasticsearch) indexing 110+ security events
  - Designed Kibana dashboards visualizing alert signatures and event type distribution
  - [GitHub Repo](https://github.com/ronankongala/suricata-ids-elk-lab)

- <b>S3 Security Auditor</b>
  - Built a Python (boto3) tool to audit AWS S3 buckets for misconfigurations
  - Performed 6 security checks per bucket covering public ACL, encryption, versioning, and logging with severity classification
  - Generated structured JSON risk reports for remediation tracking
  - [GitHub Repo](https://github.com/ronankongala/-s3-security-auditor)

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
  - [GitHub Repo](https://github.com/ronankongala/CS-5770-Software-Vulnerabilities-Security)

- <b>CY5001: Cybersecurity Technologies, Threats and Defense</b>
  - Comprehensive coursework in Linux security, cryptography, and network defense
  - Implemented GPG/PGP encryption, OpenSSL operations, digital signatures, and hybrid encryption
  - Built automated security scripts for system hardening and threat detection
  - Skills: Linux administration, Bash scripting, AES/RSA encryption, digital envelopes, log analysis
  - [GitHub Repo](https://github.com/ronankongala/CY5001-Cybersecurity-Skills)

<h2>🏆 Professional Experience</h2>

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

- **[NIELIT Cybersecurity Internship](./Cyber%20security%20NIELIT%20internship.pdf)** (Summer 2024)
  - Monitored SOC operations and analyzed security alerts
  - Configured SIEM rules and correlation policies
  - Participated in incident response exercises

- **[Quizaro Web Development](./Quizaro%20web%20development%20internship.pdf)** (Spring 2024)
  - Developed secure web applications with input validation
  - Implemented OAuth 2.0 and session management
  - Conducted security code reviews

- **[Rejolt Data Science](./Rejolt%20data%20science%20internship.pdf)** (Winter 2023)
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
  - Relevant Coursework: Software Vulnerabilities and Security (CS-5770), Cybersecurity Technologies, Threats and Defense (CY5001), Network Forensics
  - Focus: Applied cryptography, secure systems, threat analysis

- **B.Tech AI and Data Science** (2021 to 2025) -- Vardhaman College of Engineering
  - Focus: Machine Learning, Data Mining, Statistical Analysis
  - GPA: 3.8/4.0
  - Capstone: AI-based Intrusion Detection System

<h2>💼 Technical Skills</h2>

**Network Forensics**: Zeek • RITA • Wireshark • Beacon Detection • PCAP Analysis • Jupyter  
**Malware Analysis**: PEStudio • CAPA • Ghidra • YARA • CAPE Sandbox • Any.run • winpmem • Volatility 3  
**Security Tools**: Splunk • Microsoft Sentinel • Metasploit • Nmap • Burp Suite • Nessus • Suricata  
**Identity and Compliance**: Active Directory • Group Policy • Microsoft Entra ID • Microsoft Intune • Conditional Access • NIST 800-171 • CMMC  
**Cloud Security**: AWS CloudTrail • AWS Lambda • Amazon S3 • boto3 • Azure • Azure App Service  
**AI and Automation**: Claude AI • OpenAI GPT-4 • n8n • Model Context Protocol (MCP) • RAG • LLM Security • Prompt Injection Defense  
**Cryptography**: OpenSSL • GPG/PGP • AES • RSA • Digital Signatures  
**Programming**: Python • SQL • Bash • PowerShell • KQL • JavaScript  
**Platforms**: Linux • Windows Server • Docker • VMware • AWS • Azure  
**Frameworks**: MITRE ATT&CK • NIST SP 800-30 • NIST SP 800-171 • CMMC • CIS Controls • OWASP Top 10 • SOC 2  

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
