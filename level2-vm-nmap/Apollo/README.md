# Level 2 Submission: Nmap Scan Report

## 1. Lab Environment Setup
- **Attacker OS:** Kali Linux
- **Target OS:** Metasploitable
- **Virtualization Software:** Oracle VirtualBox
- **Network Mode:** Internal

## 2. Nmap Commands Executed
```bash
nmap -F -oN fast_scan.txt 192.168.50.11
nmap -sV -sC -oN service_scan.txt 192.168.50.11
```

## 3. Screenshots
![VMs Running](C:\Users\saich\CyberSec\level2-vm-nmap\Apollo\Attacker_VM.png) (C:\Users\saich\CyberSec\level2-vm-nmap\Apollo\Target_VM.png)
![Nmap Output](C:\Users\saich\CyberSec\level2-vm-nmap\Apollo\nmap_output.png)

## 4. Top 3 Findings
- **Port/Service 1:** nfs
- **Port/Service 2:** mountd
- **Port/Service 3:** nlockmgr

## 5. Security Recommendation
- **Recommendation:** Don't use Metasploitable. If using Metasploitable, make sure to enable firewall.

  Good luck and happy scanning! 🔍
