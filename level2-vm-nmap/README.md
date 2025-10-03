# Level 2: VM Lab & Nmap Scan

### **Objective**
Set up a two-machine virtual lab environment and perform basic network reconnaissance using Nmap.

---

### **Core Concepts**
- **Virtualization:** VMware or VirtualBox
- **Virtual Networking:** Host-Only (recommended) or NAT
- **Network Scanning:** Nmap basics (fast scan, service/version detection)
- **Data Redaction:** Removing sensitive info (e.g., public IPs) from submissions.

---

### **Your Tasks**

#### 1. Build the Lab
- Create two virtual machines:
  - **Attacker VM** (e.g., Kali Linux, or any distro with Nmap).
  - **Target VM** (e.g., Ubuntu, Windows, or a vulnerable machine like Metasploitable).
- Configure them on a private virtual network (Host-Only is recommended for isolation).

#### 2. Perform Scans
From your Attacker VM, run the following scans against your Target VM's private IP address.

- **Fast Scan:** To quickly identify the most common open ports.
- **Service & Version Scan:** To get detailed information about the services running on the open ports.

#### 3. Document Your Findings
Create a report that includes your lab setup, the commands you ran, your key findings, and a security recommendation based on what you discovered.

---

### **Required Deliverables**

Place all of the following files inside a new folder: `level2-vm-nmap/<your-github-handle>/`

1.  `report.md` — Your main report file.
2.  `fast_scan.txt` — The full, unedited output from your fast scan.
3.  `service_scan.txt` — The full, unedited output from your service & version scan.
4.  `screenshots/` — A folder containing at least one image, `vms_running.png`, showing both of your VMs running.

> **CRITICAL:** Before submitting, you **must** redact any public IP addresses, real usernames, or other sensitive information from your `report.md` and screenshots.

---

### **Example Nmap Commands**

Use these commands on your **Attacker VM**. Replace `<TARGET_IP>` with the private IP of your Target VM.

**Fast Scan:**
```bash
nmap -F -oN fast_scan.txt <TARGET_IP>
nmap -sV -sC -oN service_scan.txt <TARGET_IP>
```
## What to Include in report.md
Your report should be brief and clear, with the following sections:

Lab Setup: Attacker OS, Target OS, Virtualization Software, and Network Mode (Host-Only/NAT).

Commands Run: The exact commands you used.

Top 3 Findings: A short bulleted list of the most interesting open ports or services you found.

Recommendation: One concrete security recommendation for the target based on your findings.
____________________
