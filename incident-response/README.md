# 🚨 Cybersecurity Incident Response — Cybersecurity Master's Program

This module focuses on the full lifecycle of cybersecurity incident management, from asset identification and risk prioritization to technical response, CSIRT coordination, and SIEM-based monitoring.

It includes hands-on labs simulating real-world attack detection, analysis, and mitigation scenarios.

---

## 🧠 Lab Overview

These exercises demonstrate practical incident response workflows, combining technical analysis, organizational processes, and regulatory compliance to effectively handle cybersecurity incidents.

---

## 📂 Lab Summary

### 🧩 Asset Identification & Critical Infrastructure Auditing

Design of a segmented enterprise network architecture including:
- LAN  
- DMZ  
- Smart Factory environments  

Key assets identified:
- SOC servers  
- ERP systems  
- NAS storage  
- PLC and SCADA systems  

For each asset:
- Security controls defined (antimalware, access control, monitoring)  
- Applicable audits (pentesting, perimeter security, forensic and legal reviews)  
- Continuous improvement strategies using **CMMI** and **PDCA** models  

---

### ⚙️ Risk Prioritization & Incident Taxonomy

Definition of asset hierarchy across multiple layers:
- Communication  
- Services  
- Infrastructure  
- Information  

Risk analysis applied to real scenarios:

- **SOC:** Logical intrusion and compromise  
- **ERP:** DoS attacks affecting availability  
- **Inventory database:** SQL Injection impacting integrity  
- **Router:** Service disruption due to misconfiguration or attacks  

**Outcome:**  
Risk matrix and criticality analysis to prioritize incident response strategies.

---

### 🕵️ Phishing Incident & Persistence Analysis

Simulation of a phishing attack where a user executed a malicious file (`Putty.exe`).

**Findings:**
- Unauthorized active connections (port 139 / SMB)  
- Suspicious processes (`nc.exe` → Netcat backdoor)  
- Persistence mechanisms in Windows Registry:  
  `HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\Run`  
- Event Viewer errors indicating automated execution attempts  

**Forensic validation:**
- Disk integrity verified with QuickHash  
- Detection of corrupted files and header manipulation  

**Result:**  
Evidence of system compromise and tampering.

---

### 🧠 Incident Management & Response

Documentation of full incident response lifecycle:

- Detection (SIEM / IDS / log monitoring)  
- Analysis  
- Containment  
- Mitigation  
- Recovery  

**Organizational structure:**
- CISO  
- SOC team  
- IT  
- Legal  
- Executive leadership (CEO / CSO)  

**Ransomware playbook:**
- Isolation of compromised systems  
- No ransom payment policy  
- Recovery from verified backups  
- System hardening and user awareness training  

---

### 🧾 Incident Reporting & CSIRT Coordination

Creation of a realistic incident report for a web attack involving malicious code injection.

**Classification:**
- Web Attack – Malicious Code Injection  

**Severity:**
- Critical  

**Impact:**
- High risk of data exfiltration and manipulation  

**Regulatory reporting:**
- National CSIRT (CCN-CERT)  

Report includes:
- Timeline of events  
- Impact assessment  
- Mitigation measures  
- Reputational impact  
- Compliance considerations (ENS, GDPR)  

Communication phases:
- Initial notification  
- Follow-up updates  
- Incident closure  

---

### 🧩 IDS Implementation with Snort

Deployment of a lab environment including:
- Ubuntu Server  
- SOC  
- Snort IDS  
- Web server in DMZ  

Configuration:
- Internal network: `192.168.2.0/24`  
- External network: `192.168.1.0/24`  

**Custom rules created for:**
- ICMP (internal/external ping detection)  
- SSH connections  
- HTTP traffic  
- Unauthorized access attempts to `/phpmyadmin`  

**Validation:**
- Log analysis (`/var/log/snort/alert`)  
- Real traffic simulation  

---

### 📊 SIEM Monitoring with ELK Stack

Implementation of a SIEM solution using the Elastic Stack:

- **Elasticsearch:** Log storage and querying  
- **Logstash:** Data processing and pipeline creation  
- **Kibana:** Visualization dashboards  
- **Filebeat:** Log forwarding from Snort  

**Dashboards included:**
- Internal vs external ping counters  
- SSH connection attempts  
- Access attempts to phpMyAdmin  

---

## 🧰 Tools & Technologies

| Category | Tools / Technologies |
|----------|---------------------|
| **Detection & Analysis** | Snort, IDS/IPS, Nmap, Wireshark |
| **Monitoring & SIEM** | ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat) |
| **Incident Handling** | SIEM, SOC workflows, QuickHash, Event Viewer |
| **Response & Mitigation** | PDCA, CMMI, CSIRT, CCN-CERT |
| **Systems & Networking** | Ubuntu Server, Windows, DMZ, VLAN |
| **Methodologies** | Incident taxonomy, Risk management, ENS, GDPR |

---

## 🎯 Key Takeaways

These labs demonstrate the complete incident response lifecycle in realistic environments, focusing on:

- Threat detection and analysis  
- Incident classification and prioritization  
- Technical and organizational response  
- SIEM-based monitoring and visibility  
- Communication with CSIRT and regulatory compliance  

---
