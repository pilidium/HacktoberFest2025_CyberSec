# 🧪 Level 2: VM Lab & Nmap Scan

## 🎯 Objective

Set up a two-machine virtual lab environment and perform basic network reconnaissance using **Nmap**.

---

## 🧠 Core Concepts

- **Virtualization**: VMware or VirtualBox  
- **Virtual Networking**: Host-Only (recommended) or NAT  
- **Network Scanning**: Nmap basics (fast scan, service/version detection)  
- **Data Redaction**: Remove sensitive info (e.g., public IPs) before submission  

---

## 🛠️ Your Tasks

### 1. Build the Lab

- Create two virtual machines:
  - **Attacker VM**: Kali Linux or any distro with Nmap
  - **Target VM**: Ubuntu, Windows, or a vulnerable machine like Metasploitable
- Configure both on a **private virtual network** (Host-Only recommended)

### 2. Perform Scans

From your Attacker VM, run the following scans against your Target VM’s **private IP address**:

- **Fast Scan**: Quickly identify common open ports
- **Service & Version Scan**: Detect services and versions running on those ports

### 3. Document Your Findings

Create a report that includes:

- Lab setup details
- Nmap commands used
- Key findings
- One security recommendation

---

## 📦 Required Deliverables

Place all files inside a new folder:  level2-vm-nmap/<your-github-handle>/

Your folder must include:

1. `report.md` — Your main report file  
2. `fast_scan.txt` — Full output from your fast scan  
3. `service_scan.txt` — Full output from your service/version scan  
4. `screenshots/` — A folder with:
   - `vms_running.png`: Both VMs running
   - `nmap_output.png`: Attacker terminal showing Nmap output

> ⚠️ **CRITICAL**: Redact all public IPs, usernames, and sensitive info from `report.md` and screenshots before submitting.

---

## 🧪 Nmap Commands

Run these from your **Attacker VM**, replacing `<TARGET_IP>` with the private IP of your Target VM:

**Fast Scan**
```bash
nmap -F -oN fast_scan.txt <TARGET_IP>
```
```bash
Service & Version Scan
nmap -sV -sC -oN service_scan.txt <TARGET_IP>
```
### 📝  Template
Copy and paste the template below into your  and fill in the details:

# Level 2 Submission: Nmap Scan Report

## 1. Lab Environment Setup
- **Attacker OS:** ______
- **Target OS:** ______
- **Virtualization Software:** ______
- **Network Mode:** ______

## 2. Nmap Commands Executed
```bash
nmap -F -oN fast_scan.txt <REDACTED_IP>
nmap -sV -sC -oN service_scan.txt <REDACTED_IP>
```

## 3. Screenshots
![VMs Running](screenshots/vms_running.png)  
![Nmap Output](screenshots/nmap_output.png)

## 4. Top 3 Findings
- **Port/Service 1:** ______  
- **Port/Service 2:** ______  
- **Port/Service 3:** ______  

## 5. Security Recommendation
- **Recommendation:** ______

  Good luck and happy scanning! 🔍
