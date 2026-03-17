# 🔍 Digital Forensics — Cybersecurity Master's Program

Collection of hands-on labs developed during the **Digital Forensics** module of my Professional Master's Degree in Cybersecurity.

This repository includes practical exercises covering memory analysis, mobile forensics, cloud investigations, IoT firmware analysis, and forensic reporting.

---

## 🧠 Overview

These labs demonstrate the application of real-world forensic methodologies for the acquisition, preservation, and analysis of digital evidence.

The objective is to combine technical techniques with legal and procedural standards (e.g., chain of custody, TLP classification) to produce reliable and reproducible results in investigative contexts.

---

## 📂 Lab Summary

### 🖥️ Memory Analysis (RAM — Server)

**Objective:**  
Analyze a volatile memory image to identify malicious activity and attacker behavior.

**Tools:**  
Volatility (v2), FTK Imager  

**Key Techniques:**  
- `imageinfo`, `pslist`, `cmdscan`, `netscan`, `malfind`

**Key Findings:**  
- Identification of attacker commands (user creation, RDP enablement)  
- Detection of injected code and indicators of fileless malware  

**Value:**  
Ability to extract Indicators of Compromise (IPs, processes, commands) from RAM before system shutdown.

---

### 📱 iOS Backup Extraction & Analysis

**Objective:**  
Acquire and analyze a logical backup from an iPhone to extract forensic artifacts.

**Tools:**  
iTunes, Magnet Acquire, iLEAPP, iBackup Viewer  

**Key Techniques:**  
- Logical extraction (backup)  
- Artifact parsing with iLEAPP  
- Permissions and application data inspection  

**Key Findings:**  
- Structured forensic report generation  
- Identification of potential integrity risks due to system processes  

**Value:**  
Understanding workflows for evidence extraction in mobile environments where full physical access is not available.

---

### ☁️ Cloud Forensics Considerations

**Objective:**  
Evaluate challenges and requirements for conducting forensic investigations in cloud environments.

**Key Concepts:**  
- Data sovereignty  
- Log accessibility  
- Shared responsibility model (SLA)  
- GDPR compliance  
- Data portability (Art. 20)

**Key Findings:**  
Minimum requirements for forensic readiness in cloud providers:
- Detailed logging  
- Accessible backups  
- Audit capabilities  
- Contractual guarantees  

**Value:**  
Understanding legal and operational limitations of cloud forensic investigations.

---

### 💡 IoT Firmware Forensics

**Objective:**  
Extract and analyze firmware from IoT devices (e.g., smart bulb, camera) to identify services, users, and misconfigurations.

**Tools:**  
binwalk, unsquashfs, Jefferson, grep  

**Key Techniques:**  
- Filesystem identification (SquashFS, JFFS2)  
- Extraction of `/etc`  
- Analysis of `mosquitto.conf`  
- User enumeration (`/etc/passwd`)  

**Key Findings:**  
- MQTT communication without authentication (`allow_anonymous true`) → critical risk  
- Identification of embedded services (BusyBox, web server, DHCP)  
- Embedded Linux (ARM) with boot configuration (`boot.sh`)  

**Value:**  
Demonstrates how firmware analysis reveals system configuration and potential attack vectors in IoT devices.

---

### 🧾 Forensic Reporting & Chain of Custody

**Objective:**  
Evaluate and produce forensic reports with proper structure, clarity, and legal validity.

**Key Concepts:**  
- Chain of custody  
- Traffic Light Protocol (TLP)  
- Separation of facts vs hypotheses  
- Executive summary clarity  

**Key Findings:**  
- Recommendations for reproducibility improvements  
- Inclusion of hashes and evidence tables  
- Proper TLP classification (e.g., TLP:AMBER)  

**Value:**  
Ability to translate technical findings into legally sound and clearly communicated forensic reports.

---

## 🧰 Tools & Technologies

| Category | Tools / Concepts |
|----------|----------------|
| **Memory Analysis** | Volatility, FTK Imager |
| **Mobile Forensics** | iLEAPP, iBackup Viewer, Magnet Acquire |
| **IoT Firmware** | Binwalk, unsquashfs, Jefferson |
| **Data Processing** | jq, grep, Python scripts |
| **Methodology & Standards** | TLP, Chain of Custody, GDPR, Log Analysis |

---

## 🎯 Key Takeaways

These labs reflect real-world application of forensic techniques across multiple environments, focusing on:

- Evidence integrity  
- Process traceability  
- Legal compliance  
- Reproducibility of results  

---
