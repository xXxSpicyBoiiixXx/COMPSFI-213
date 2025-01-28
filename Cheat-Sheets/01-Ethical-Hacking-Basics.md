# Chapter 01: Ethical Hacking Basics

## Overview
This cheat sheet provides essential commands for ethical hacking and reconnaissance, focused on tools and techniques introduced in Chapter 01.

## Commands

### **Network Enumeration**
- **Whois**: Gather domain registration information.
  ```bash
  whois [domain]
  ```
- **Ping**: Test connectivity to a host.
  ```bash
  ping [IP/Domain]
  ```

### **Port Scanning**
- **Nmap**: Scan for open ports and services.
  - Basic port scan:
    ```bash
    nmap [IP/Range]
    ```
  - SYN (stealth) scan:
    ```bash
    nmap -sS [IP]
    ```
  - Aggressive scan (OS and service detection):
    ```bash
    nmap -A [IP]
    ```
  - Scan specific ports:
    ```bash
    nmap -p [port] [IP]
    ```

### **Reconnaissance**
- **Netstat**: View open ports and active connections.
  - Show all open ports with process IDs:
    ```bash
    netstat -ano
    ```
  - Display routing table:
    ```bash
    netstat -r
    ```

## Best Practices
- Use tools responsibly and only on systems where you have explicit permission.
- Always adhere to ethical and legal standards during testing.
