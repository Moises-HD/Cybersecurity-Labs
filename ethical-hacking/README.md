# 🧠 Ethical Hacking — Cybersecurity Master's Program

This module focuses on identifying, exploiting, and mitigating vulnerabilities in IT systems using professional penetration testing methodologies.

It includes hands-on labs covering security auditing, wired and wireless network pentesting, vulnerability exploitation, and web application security testing.

---

## 🧠 Lab Overview

These exercises demonstrate controlled offensive security techniques applied in realistic environments, with the goal of understanding attacker behavior and strengthening defensive strategies.

---

## 📂 Lab Summary

### 🧩 Security Audit Planning & Execution

Design and execution of a cybersecurity audit plan based on real-world scenarios:

- **External testing (Black Box):**  
  Simulating attacks from the internet  

- **Internal testing (Grey Box):**  
  Evaluating threats from within the corporate network  

- **Red Team simulations:**  
  Combining reconnaissance, exploitation, and lateral movement  

Defined audit phases:
- Requirements  
- Testing  
- Reporting  
- Closure  

**Vulnerability assessment using CVSS metrics**

**Key vulnerabilities identified:**
- Remote Code Execution (RCE) in mail server  
- SQL Injection in web applications  
- Code execution in internal FTP server  

Each vulnerability was evaluated in terms of:
- Impact  
- Exploitability  
- Mitigation  

---

### 📡 Corporate Wi-Fi Security Assessment

Evaluation of three wireless network configurations:

- **OPEN network:**  
  No encryption → high risk (interception, spoofing)  

- **WPA2-PSK:**  
  Shared key → lack of traceability and device control  

- **WPA2-Enterprise:**  
  Stronger authentication but requires proper policy enforcement  

**Recommended countermeasures:**
- Migration to WPA3-Enterprise  
- Implementation of MDM  
- VLAN segmentation  
- Strict certificate validation  
- Continuous monitoring and credential rotation  

---

### 💻 Pentesting Phases with Metasploit

Lab environment using **Kali Linux** and **Metasploitable 2**:

- **Reconnaissance:**  
  Advanced dorking techniques (Google Hacking)  

- **Scanning:**  
  Service and port discovery (`nmap -sV`)  

- **Vulnerability identification:**  
  Using `vulscan`  

- **Exploitation:**  
  Metasploit module `vsftpd_234_backdoor`  

**Result:**  
Successful remote access to the target system and full understanding of a controlled attack lifecycle.

---

### 🧠 Password Cracking & Persistence (Windows Environment)

Lab setup with **Windows 7** and **Kali Linux**:

- **Password cracking with Hashcat**, using:
  - MD5 (`-m 0`)  
  - NTLM (`-m 1000`)  
  - NETNTLMv2 (`-m 5600`)  
  - Kerberos TGS (`-m 13100`)  

- **Exploitation:**  
  EternalBlue (MS17-010) via Metasploit  

- **Post-exploitation persistence:**  
  - Windows services (`sc create`)  
  - Registry modifications (`reg add`)  

**Result:**  
Simulation of advanced Red Team attack scenarios in Windows environments.

---

### 🌐 Web Vulnerabilities & Testing with Burp Suite

Security testing of vulnerable web applications using:

- Burp Suite  
- DVWA  
- SQLMap  

**Attacks performed:**

- **Brute force attacks:**  
  Login forms via Burp Intruder  

- **Stored XSS:**  
  Script execution in user browsers  

- **Remote Command Execution (RCE):**  
  Parameter injection  

- **SQL Injection:**  
  Database extraction using SQLMap  

**Objective:**  
Understand OWASP Top 10 vulnerabilities and their real-world impact, along with mitigation strategies.

---

## 🧰 Tools & Technologies

| Category | Tools / Technologies |
|----------|---------------------|
| **Pentesting & Exploitation** | Metasploit, Nmap, Vulscan, Netcat |
| **Password Cracking** | Hashcat, RockYou, John the Ripper |
| **Web Security Testing** | Burp Suite, DVWA, SQLMap |
| **Wireless Networks** | WPA2/WPA3, RADIUS, Wireshark |
| **Operating Systems** | Kali Linux, Windows 7, Metasploitable 2 |
| **Methodologies** | OWASP, CVSS, Red Team / Blue Team |

---

## 🎯 Key Takeaways

These labs demonstrate the controlled application of offensive and defensive security techniques, focusing on:

- Vulnerability discovery and exploitation  
- Attack lifecycle understanding  
- Real-world pentesting workflows  
- Security posture improvement  

---
