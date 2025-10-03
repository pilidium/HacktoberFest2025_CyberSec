# Level 2 Submission: Nmap Scan Report

## 1. Lab Environment Setup

**Attacker VM**  
- OS: Kali Linux 2023.4  
- Network Mode: Host-Only  
- IP: `192.168.56.101`

**Target VM**  
- OS: Metasploitable 2 (Linux)  
- Network Mode: Host-Only  
- IP: `192.168.56.102`

> **Note:** These are private lab IPs — redact if making public.

---

## 2. Nmap Commands Executed

```bash
nmap -F 192.168.56.102
nmap -sV -sC 192.168.56.102
```
## 3. Findings

Port 21/tcp: vsftpd 2.3.4

Port 23/tcp: Linux telnetd

Port 80/tcp: Apache httpd 2.2.8 ((Ubuntu) DAV/2)
