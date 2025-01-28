# Chapter 02: TCP/IP and Network Protocols

## Overview
This cheat sheet provides essential commands related to TCP/IP, IP addressing, and network troubleshooting, focusing on tools and techniques introduced in Chapter 02.

## Commands

### **Inspecting TCP/IP**
- **Netstat**: Examine active TCP connections.
  - Show active connections:
    ```bash
    netstat -an
    ```
  - Display TCP statistics:
    ```bash
    netstat -s
    ```

### **Testing Connections**
- **Ping**: Verify connectivity to a host.
  ```bash
  ping [IP/Domain]
  ```
- **Traceroute**: Trace the path packets take to a destination.
  - **Linux/Mac**:
    ```bash
    traceroute [IP/Domain]
    ```
  - **Windows**:
    ```bash
    tracert [IP/Domain]
    ```

### **IP Address Management**
- **Ifconfig** (Linux/Mac): Display or configure IP addresses.
  - Show IP configuration:
    ```bash
    ifconfig
    ```
  - Enable or disable a network interface:
    ```bash
    ifconfig [interface] up/down
    ```
- **Ipconfig** (Windows): View network configuration.
  - Show full configuration:
    ```bash
    ipconfig /all
    ```
  - Clear DNS cache:
    ```bash
    ipconfig /flushdns
    ```

### **DNS Queries**
- **Dig**: Query DNS servers for information (Linux/Mac).
  ```bash
  dig [domain]
  ```

### **Port Scanning**
- **Nmap for Ports**:
  - Scan specific ports:
    ```bash
    nmap -p [port] [IP]
    ```
  - Example:
    ```bash
    nmap -p 80,443 192.168.1.1
    ```

### **Common Email Ports**
- **SMTP (Port 25)**: Sending emails.
- **POP3 (Port 110)**: Retrieving emails.
- **IMAP (Port 143)**: Advanced email retrieval.

### **Subnet and IP Planning**
- CIDR notation for subnet masks:
  - Example: `192.168.1.0/24` (Class C).

### **ICMP Tools**
- **Ping**: Send ICMP echo requests to test connectivity.
- **Traceroute/Tracert**: Diagnose network paths and latency.

## Best Practices
- Ensure compliance with local laws before using these tools.
- Use tools on systems or networks where you have permission.


