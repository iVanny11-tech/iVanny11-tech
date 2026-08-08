<div align="center">

# IVAN YAMOAH BOAKYE
### Security Operations Analyst &nbsp;|&nbsp; IT Support Specialist

*Building real enterprise SOC workflows — detection engineering, incident response, threat hunting, and cloud security across Microsoft and Fortinet platforms.*

<br>

<a href="https://www.linkedin.com/in/ivanboakye121"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:yivan56@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://github.com/iVanny11-tech"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"/></a>

</div>

---

## Quick Stats

- 7+ hands-on security labs documented end-to-end with screenshots
- Built a full Microsoft SOC simulation — Sentinel · Defender XDR · Entra ID Protection · Azure Arc
- Fortinet NSE 4 certified | Pursuing NSE 5 and SC-200
- Hands-on with FortiGate, FortiAnalyzer, Microsoft Sentinel, Defender XDR, and Azure
- Based in Toronto — open to remote, hybrid, and onsite roles across the GTA

---

## Project Portfolio

---

### Phase 1 — Microsoft SOC & Azure Security

---

<h3><a href="https://github.com/iVanny11-tech/soc-lab-microsoft-sentinel">01 — Project ATLAS: Microsoft SOC Tier 1/2 Simulation</a></h3>

**Incident Response & Detection Engineering | Microsoft Sentinel + Defender XDR + Entra ID Protection**

Built a hybrid SOC lab using VirtualBox (Kali + Windows 11 ARM64), Azure Arc, Sysmon, and the Azure Monitor Agent. Simulated a full MITRE ATT&CK attack chain and performed end-to-end incident response.

- Simulated 5 ATT&CK techniques: RDP brute force, encoded PowerShell, spearphishing, Tor sign-in, and valid cloud account abuse
- Built custom KQL analytics rules in Sentinel — brute force (EID 4625) and encoded PowerShell via Sysmon EID 1
- Triaged Defender XDR Incident ID 2 — High severity, 8 correlated alerts — classified as True Positive: Compromised Account
- Performed hypothesis-driven threat hunt and discovered a full AMA telemetry pipeline failure
- Contained endpoint with `netsh advfirewall`; remediated via Entra ID Protection confirmCompromised
- Created Conditional Access policy blocking anonymous IP sign-in risk (Tor exit nodes)

**Tools:** Microsoft Sentinel | Defender XDR | Entra ID P2 | Azure Arc | Sysmon | KQL | Hydra | Kali Linux

---

<h3><a href="https://github.com/iVanny11-tech/soc-tier1-alert-triage-phishing-automation">02 — Project BEACON: Tier 1 SOC Analyst Simulation</a></h3>

**Alert Triage & Phishing Investigation | Microsoft Sentinel + Jira Service Management + Python Automation**

Built a single-session Tier 1 SOC analyst simulation covering alert triage, escalation, and phishing investigation on the same Azure backend as Project ATLAS, plus a custom Python SOAR-style automation pipeline.

- Triaged 5 alert types (port scans, RDP brute-force burst, benign/encoded PowerShell) against a written playbook with a documented decision tree
- Escalated 2 true positives with SHA256 hash verification (VirusTotal) and event-timeline reconstruction from Windows Security logs
- Investigated 2 phishing simulations (Credential Harvest, Link in Attachment) via Defender Attack Simulation Training without detonating payloads
- Built a custom Python IOC enrichment pipeline (VirusTotal + AbuseIPDB APIs, weighted risk scoring) — a lightweight SOAR playbook prototype
- Diagnosed a broken Azure Monitor Agent telemetry pipeline, distinguishing Arc connectivity from telemetry shipping as independently-failing systems

**Tools:** Microsoft Sentinel | Jira Service Management | KQL | PowerShell | Python | VirusTotal API | AbuseIPDB API | Defender Attack Simulation Training

---

### Phase 2 — Fortinet Network Security

---

<h3><a href="https://github.com/iVanny11-tech/fortinet-security-labs">03 — FortiGate IPS Lab</a></h3>

**Threat Detection & Prevention | FortiGate + FortiAnalyzer**

- Built a custom IPS sensor targeting CVE-based HTTP exploit signatures
- Configured Virtual IPs (VIPs) for inbound NAT and policy enforcement
- Simulated real attacks using Nikto web scanner against a live target
- Analysed triggered alerts in FortiAnalyzer with CLI diagnostics
- Documented full topology with inline screenshots per step

**Tools:** FortiGate | FortiAnalyzer | Nikto | CLI Diagnostics

---

<h3><a href="https://github.com/iVanny11-tech/fortianalyzer-log-management-fortiview">04 — FortiAnalyzer Log Management & FortiView</a></h3>

**Log Analysis & Threat Investigation | FortiAnalyzer + FortiView**

- Imported historical FortiGate log files and generated live traffic for analysis
- Drilled into raw log records — decoding srcip, dstip, policyid, action, and sessionid fields
- Built a custom saved view for Application Control logs (P2P and cloud storage activity)
- Configured a server-scoped IPS sensor; simulated a real Nikto web attack
- Traced the attack in FortiView Top Threats — source IP, threat score, and technique
- Validated FortiAnalyzer health via CLI: log insertion rate, per-device storage, and lag time

**Tools:** FortiAnalyzer | FortiView | FortiGate | Nikto | PuTTY | CLI Diagnostics

---

### 05 — Enterprise Active Directory Infrastructure: Deployment, Administration & Incident Response

Enterprise AD Deployment & Incident Response | AWS + Windows Server 2022 + Active Directory Domain Services

Built and operated a full enterprise Active Directory environment on AWS from the ground up — cloud infrastructure, domain services, departmental OU/user/group design, GPO security hardening, and a Windows client domain-join that surfaced three real, unplanned incidents diagnosed and resolved live.

- Provisioned AWS VPC, subnets, security groups, and EC2-hosted domain controller (DC01) running Windows Server 2022 + AD DS
- Designed 8 Organizational Units and departmental structure across IT, HR, Finance, and Sales, with security groups, NTFS permissions, and SMB file shares scoped per department
- Hardened the environment via Group Policy — password policy, account lockout policy, screen lock timeout, USB restriction, update deferral, and automated drive mapping
- Ran a simulated help-desk ticket queue via PowerShell — account unlocks, password resets, onboarding, and offboarding
- Diagnosed and resolved 3 real incidents: an RDP security-group misconfiguration, an AWS Systems Manager limitation on domain controllers, and a cascading DNS → security-group → account-lockout failure during a client domain-join that also cut off admin access to the DC itself
- Regained locked-out domain controller access via AWS's key-pair-based local Administrator credential recovery, independent of the domain account

**Tools:** AWS (EC2, VPC, Security Groups, Systems Manager, IAM) | Windows Server 2022 | Active Directory Domain Services | Group Policy Management | PowerShell | DNS | NTFS/SMB

**Repo:** [enterprise-AD-infrastructure](https://github.com/iVanny11-tech/enterprise-AD-infrastructure)



### Phase 6 — Cloud & DevOps Security

---

<h3><a href="https://github.com/iVanny11-tech/aws-ec2-nginx-dns-project">07 — AWS EC2 Nginx + DNS</a></h3>

**Web Server Deployment | AWS EC2 + Route 53**

- Deployed NGINX web server on AWS EC2 connected to a custom domain via Route 53
- Configured security groups and IAM access controls

**Tools:** AWS EC2 | NGINX | Route 53 | IAM

---

<h3><a href="https://github.com/iVanny11-tech/AWS-TIER-2-WEB-APP">06 — AWS Web Tier 2 Application</a></h3>

**Multi-Tier Architecture | AWS**

- Designed and deployed a multi-tier web application on AWS
- Implemented network segmentation across public and private subnets

**Tools:** AWS VPC | EC2 | Security Groups | Subnetting

---

### Phase 8 — SOC Analyst & SIEM (In Progress)

---

### 08 — Splunk SIEM Home Lab *(Coming Soon)*

**Security Monitoring | Splunk + SPL**

- Ingesting Linux auth logs and building SPL detection queries
- Detecting brute force SSH, privilege escalation, and suspicious login patterns
- Building dashboards and custom alerts

**Tools:** Splunk | SPL | Ubuntu | Linux Auth Logs

---

### 09 — Wazuh SIEM & EDR Lab *(Coming Soon)*

**SIEM + EDR | Wazuh + VirtualBox**

- Deploying Wazuh manager and agent on Ubuntu VM
- Configuring custom detection rules and alert thresholds
- Simulating phishing and endpoint compromise scenarios

**Tools:** Wazuh | VirtualBox | Ubuntu | Gophish

---

## Technical Skills

| Category | Tools & Technologies |
|---|---|
| **SIEM & Detection Engineering** | Microsoft Sentinel, Defender XDR, Wazuh, Splunk, FortiAnalyzer |
| **Firewall & Network Security** | FortiGate, FortiAnalyzer, FortiManager, VIPs, IPS, SD-WAN |
| **Cloud Security** | Microsoft Azure, Entra ID P2, Azure Arc, AWS EC2, IAM, KQL |
| **Identity & Access** | Entra ID Protection, Conditional Access, Azure AD, IAM, RBAC |
| **EDR & Endpoint** | CrowdStrike Falcon, Darktrace, Microsoft Purview |
| **Threat Simulation** | Hydra, Nmap, Nikto, M365 Attack Simulation Training, Tor |
| **Scripting & Automation** | Python, Bash, KQL, CLI |
| **Operating Systems** | Windows, Ubuntu Linux, Kali Linux, macOS |

---

## Certifications & Training

| Certification | Status |
|---|---|
| CompTIA Security+ | Completed |
| Fortinet NSE 1, 2, 3 | Completed |
| Fortinet NSE 4 — FortiOS 7.6 Administrator | Completed |
| Microsoft AI Skills Fest 2026 | Completed |
| Fortinet NSE 5 — FortiAnalyzer SOC Analyst | In Progress |
| Microsoft SC-200 — Security Operations Analyst | In Progress |

---

<div align="center">

**Targeting:** SOC Analyst /IT SUPPORT &nbsp;·&nbsp; Cloud Security Engineer &nbsp;·&nbsp; SecOps Roles

Toronto, Ontario — Remote & Hybrid Welcome

</div>
