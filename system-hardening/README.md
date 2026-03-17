# 🔒 Network & System Hardening — Cybersecurity Master's Program

This module focuses on securing and hardening networks, servers, and operating systems by applying modern security principles such as Zero Trust, network segmentation, multi-factor authentication, and secure service configuration.

---

## 🧠 Lab Overview

These labs demonstrate practical implementation of defensive security strategies aimed at reducing attack surface, preventing lateral movement, and enforcing strong access control mechanisms across systems and networks.

---

## 📂 Lab Summary

### 🔐 Zero Trust Paradigm

Analysis of the Zero Trust security model, where no user or system is trusted by default.

Reference solutions explored:
- Zscaler Zero Trust Exchange  
- Fortinet ZTA  

Implementation concepts:
- Identity-based access control  
- Context-aware policies  
- Microsegmentation  

**Objective:**  
Minimize attack surface and prevent lateral movement within the network.

---

### 🧱 Security Audit & Hardening Proposal (Enterprise Scenario)

Evaluation of a fictional company (**Venus S.A.**) identifying critical weaknesses:
- Lack of environment separation  
- Weak access control  
- Poor physical server placement  

**Mitigation strategies:**
- Segregation of services (web, internal systems, backups)  
- Role-based access control (RBAC) and least privilege  
- Security policies, audits, and skilled personnel  

---

### 🔑 2FA & MFA Authentication

Comparison of two-factor and multi-factor authentication mechanisms.

**Examples:**
- Gmail / Facebook (SMS / authenticator apps)  
- Online banking (hardware tokens)  

**Conclusion:**  
Significantly reduces unauthorized access at the cost of increased operational complexity.

---

### 📡 RADIUS Server Implementation

Configuration of a **FreeRADIUS server** on Ubuntu for Wi-Fi authentication using **WPA2-Enterprise**.

Key steps:
- Client definition (`clients.conf`)  
- Authentication configuration with `hostapd`  

Even without physical hardware, the full setup and validation process was documented.

---

### 🧩 MAC Filtering & IDS with Snort

- MAC address filtering in a home router  
- MAC spoofing in Ubuntu for controlled testing  

Deployment of **Snort (IDS)** to:
- Monitor network traffic  
- Detect scans using Nmap (Kali Linux)  

**Results:**
- Detection of suspicious activity via logs (`snort.alert.fast`)  
- Validation of IDS rules effectiveness  

---

### 🕸️ Network Segmentation with VLANs & DMZ

Design of a segmented network architecture using VLANs:
- VLAN 10: Critical services  
- VLAN 20: Management  
- VLAN 30: Employees  
- VLAN 40: Public network  

Implementation of a **DMZ** with:
- Web server  
- DNS  
- VPN  

Protected by:
- Perimeter firewall  
- Internal firewall  

**Security measures:**
- Access rules by IP, port, and protocol  
- Cloud security (TLS, 2FA, CASB, backups)  

---

### ⚔️ DDoS & Web Attack Analysis

Analysis of Apache, SSH, and FTP logs to detect:
- DDoS attempts  
- Brute-force attacks  
- Data exfiltration  

**Findings:**
- Internal attacker (`192.168.10.5`) performing scans (Nmap) and anonymous FTP access  

**Countermeasures:**
- Temporary blocking  
- Real-time monitoring  
- Firewall log analysis for traceability  

---

### 🧮 Linux Security Auditing & Permissions Review

Detection of insecure configurations and privilege escalation vectors:

- `find / -perm` for insecure permissions  
- GTFOBins exploitation vectors  
- `$PATH` vulnerabilities  
- Insecure shared directories  
- `/etc/fstab` mount options  
- Secure file deletion (`shred`)  

**Objective:**  
Eliminate unsafe configurations enabling unauthorized execution or access.

---

### 🧰 SSH Hardening & Remote Access Control

Implementation of advanced SSH security configurations:

- Disable root login  
- Session timeout (5 minutes)  
- Public/private key authentication  
- User and IP restrictions  
- Disable port forwarding & X11 forwarding  
- Secure protocols (SSH v2, SHA2-512/256)  
- Logging in `/var/log/auth.log` (SOC integration)  

**Result:**  
Secure encrypted connections, strong authentication, and full activity traceability.

---

## 🧰 Tools & Technologies

| Category | Tools / Technologies |
|----------|---------------------|
| **Networking & Segmentation** | VLANs, DMZ, Firewalls, Reverse Proxy |
| **Authentication & Access Control** | FreeRADIUS, WPA2-Enterprise, 2FA/MFA |
| **Monitoring & Detection** | Snort, Nmap, UFW, IDS/IPS |
| **Security Auditing** | GTFOBins, find, chmod, fstab, whois |
| **Protocols & Encryption** | SSH, TLS, HTTPS, SHA2 |
| **Security Models** | Zero Trust, Perimeter Security, Least Privilege |

---

## 🎯 Key Takeaways

These labs demonstrate the practical application of system and network hardening strategies in realistic environments, focusing on:

- Defense in depth  
- Network segmentation  
- Strong authentication  
- Least privilege principle  
- Continuous monitoring and auditing  

---
