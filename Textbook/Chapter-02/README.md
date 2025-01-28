# Chapter 02: TCP/IP Concepts Review

## Overview

Understanding TCP/IP is critical for ethical hacking and network defense. It forms the foundation of how computers communicate over the internet and within local networks. This chapter covers the basics of TCP/IP, IP addressing, and various numbering systems.

## Key Concepts and Objectives

By the end of this chapter, you will be able to:

1. **Explain the TCP/IP Protocol Stack**
   - Understand the four layers: Network, Internet, Transport, and Application.
   - Learn how each layer contributes to data communication.

2. **Explain the Basics of IP Addressing**
   - Understand IPv4 structure, classes (A, B, C), and subnetting.
   - Introduction to IPv6 and its advantages over IPv4.

3. **Understand Numbering Systems**
   - Binary, Octal, Hexadecimal, and Base-64 systems and their applications.

## TCP/IP Protocol Stack

1. **Application Layer**
   - Provides protocols for user interaction, such as HTTP, FTP, and DNS.
   - Visible and interactive to end-users.

2. **Transport Layer**
   - Manages data encapsulation into segments.
   - Uses TCP (connection-oriented) and UDP (connectionless) protocols.
   - Includes the TCP three-way handshake: SYN → SYN-ACK → ACK.

3. **Internet Layer**
   - Routes packets using logical IP addresses.
   - Includes protocols like IP, ICMP, and ARP.
   - Utilizes tools like `ping` and `traceroute` for network troubleshooting.

4. **Network Layer**
   - Handles physical transmission of data packets across the network.

## TCP and UDP Details

- **TCP Flags**
  - Key flags include SYN, ACK, PSH, URG, RST, and FIN.
  - Used to establish and terminate connections.
- **UDP**
  - Faster, connectionless protocol used in applications like DNS and video streaming.

## TCP Ports

- Ports are logical connections used for specific services:
  - Port 20/21: FTP
  - Port 22: SSH
  - Port 25: SMTP
  - Port 80: HTTP
  - Port 443: HTTPS
  - Full list of well-known ports available at [IANA](https://www.iana.org).

## IP Addressing

1. **IPv4 Structure**
   - Composed of four octets (e.g., 192.168.1.1).
   - Divided into Network and Host portions.

2. **Address Classes**
   - Class A: Large organizations (e.g., 10.0.0.0).
   - Class B: Medium-sized networks (e.g., 172.16.0.0).
   - Class C: Small networks (e.g., 192.168.0.0).

3. **Subnetting**
   - Used to divide networks into smaller segments for efficiency and security.

4. **IPv6**
   - Designed to replace IPv4 with a larger address space and improved security.
   - Uses 128-bit addresses (e.g., 2001:0db8::1).

## Numbering Systems

- **Binary**
  - Base-2 system; foundational to computing.
  - Each bit represents a power of 2.
- **Octal**
  - Base-8 system used in file permissions (e.g., `chmod` command in Linux).
- **Hexadecimal**
  - Base-16 system; often used in IP addressing and memory locations.
- **Base-64**
  - Encoding system for transporting binary files via email or other text-based systems.

## Practical Tools

- **Commands**
  - `netstat`: Displays open ports and connections.
  - `ipconfig`/`ifconfig`: Displays network configuration.
  - `ping`: Tests connectivity to a specific IP address.
  - `traceroute`: Tracks the path packets take to a destination.

## Summary

In this chapter, you learned the basics of TCP/IP, IP addressing, and numbering systems, which are essential for understanding how networks operate. These concepts are fundamental for identifying vulnerabilities and defending against attacks.
