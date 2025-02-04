# Chapter 03: Network and Computer Attacks

## Overview

This module provides an in-depth look at network and computer attacks, focusing on **malicious software (malware), network intrusions, and physical security vulnerabilities**. Cyber threats are evolving daily, and understanding these attacks is crucial for ethical hackers and cybersecurity professionals. The module also emphasizes **preventive and defensive measures** that organizations can implement to mitigate risks.

## Module Objectives

By the end of this module, you should be able to:
- **Understand malware threats**: Differentiate between viruses, worms, Trojans, and spyware, and recognize their impact.
- **Explain protection methods**: Identify key tools and strategies to defend against malware attacks.
- **Identify network attacks**: Learn about common attacks like DoS, buffer overflows, and session hijacking.
- **Recognize physical security vulnerabilities**: Explore risks such as keyloggers and unauthorized access.
- **Implement security countermeasures**: Understand both technical and human-centered approaches to securing systems.

---

## 1. Malicious Software (Malware)

### **What is Malware?**
Malware refers to **malicious software** designed to disrupt, damage, or gain unauthorized access to a system. Attackers use malware to **steal data, control systems, or carry out espionage**.

### **Common Types of Malware**
| Type | Description | Example |
|------|------------|---------|
| **Viruses** | Attach themselves to host files and spread via email or downloads. Require execution by a user. | Ransomware, Macro Viruses |
| **Worms** | Self-replicating malware that spreads across networks without user intervention. | Stuxnet, Code Red, Conficker |
| **Trojans** | Disguised as legitimate software but contain malicious code. Often used to install backdoors. | Zeus, Back Orifice |
| **Spyware** | Monitors user activity and sends data (keystrokes, credentials) to attackers. | Keyloggers, Screen Scrapers |
| **Adware** | Unwanted software that displays intrusive ads and collects user data. | Browser Hijackers |

### **Defense Strategies**
- **Antivirus Software**: Detects and removes malware based on known signatures.
- **Sandboxing**: Runs suspicious files in an isolated environment to observe behavior.
- **User Education**: Training on phishing emails and safe browsing habits.
- **Regular Updates**: Keeping antivirus and operating systems up to date to patch vulnerabilities.

---

## 2. Network and Computer Attacks

### **Denial-of-Service (DoS) & Distributed DoS (DDoS)**
DoS and DDoS attacks **overload network resources**, making services unavailable. Attackers may use **botnets** to generate massive traffic.

- **Example:** Ping of Death – Sending oversized ICMP packets to crash a target system.
- **Defense:** Rate limiting, firewalls, and intrusion detection systems (IDS).

### **Buffer Overflow Attacks**
Exploits **poorly written software** that does not properly manage memory. Attackers **inject malicious code** that executes with high-level privileges.

- **Example:** Exploiting a vulnerable application to gain **remote shell access**.
- **Defense:** Secure coding practices, using **address space layout randomization (ASLR)**.

### **Eavesdropping & Man-in-the-Middle (MITM) Attacks**
Attackers intercept and manipulate data between two parties.

- **Example:** A hacker using **Wireshark** to capture unencrypted passwords on a public Wi-Fi.
- **Defense:** Enforce **encrypted communication protocols (TLS, HTTPS, VPNs).**

### **Session Hijacking**
An attacker takes over a user's session by **stealing authentication tokens**.

- **Example:** Session fixation attack where an attacker **forces a victim to use a known session ID**.
- **Defense:** Implement **secure session management** (short session timeouts, HTTPS enforcement).

---

## 3. Physical Security Attacks

### **Keyloggers**
Software or hardware used to capture **keystrokes** on a computer to steal credentials.

- **Example:** USB keyloggers installed on a victim’s computer.
- **Defense:** Use **virtual keyboards**, **multi-factor authentication (MFA)**, and endpoint security.

### **Unauthorized Physical Access**
A large percentage of attacks come from **inside an organization**. Weak physical security measures can allow **insiders** to install backdoors or steal data.

- **Example:** Tailgating (following an employee into a secure area without authentication).
- **Defense:** **Biometric authentication, access logs, and security badges.**

---

## 4. Best Practices for Defense

### **User Education**
- Conduct regular security training for employees.
- Teach users how to identify **phishing emails** and **social engineering tactics**.
- Enforce **secure password policies**.

### **Updating Security Measures**
- Enable **automatic antivirus updates**.
- Regularly patch **operating systems and applications** to fix vulnerabilities.
- Use **whitelisting** to only allow approved programs to run.

### **Avoiding Fear Tactics**
- Security awareness training should focus on **education, not fear**.
- Users should feel empowered to report security incidents.

---

## 5. Assessment & Discussion Activities

### **Knowledge Check Questions**
- **What is the primary goal of malware?** *(Answer: Financial gain or destruction)*
- **Which type of attack exploits a software vulnerability to execute unauthorized code?** *(Answer: Buffer Overflow)*

### **Discussion Activity**
- Research five free antivirus solutions (e.g., **Avira, Panda, TotalAV, Kaspersky, Malwarebytes**).
- Compare their **features, effectiveness, and ease of use**.
- Discuss which **antivirus software** is the best and why.

---

## 6. Summary

By completing this module, you should now be able to:
✅ Describe **various types of malware** and their damage potential.  
✅ Implement **defensive measures** against malware and cyber attacks.  
✅ Recognize **common network attack types** and their countermeasures.  
✅ Understand **physical security threats** and how to mitigate them.  

### **Next Steps**
- Review case studies on **real-world cyber attacks**.
- Practice **hands-on malware analysis** using sandbox environments.
- Experiment with **penetration testing tools** (e.g., Metasploit, Wireshark).

