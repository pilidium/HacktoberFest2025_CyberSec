# Level 2: VM Lab & Nmap Scan

**Objective**  
Set up a two-machine virtual lab environment and perform basic network reconnaissance using Nmap.

---

## Core Concepts
- **Virtualization:** VMware, VirtualBox (choice is yours)  
- **Virtual Networking:** Host-Only (recommended), NAT  
- **Network Scanning:** Nmap basics (fast scan, service/version detection, default scripts)  
- **Command-Line Basics**  
- **Data Redaction:** remove/redact public IPs or any personal info before submission

---

## Tasks
### 1. Build the Lab
- Create two VMs:
  - **Attacker VM** (e.g., Kali Linux or any distro with Nmap)
  - **Target VM** (e.g., Ubuntu, Windows, or intentionally vulnerable image)
- Configure the VMs to communicate on a private virtual network. **Host-Only** is recommended for isolation.

### 2. Perform Scans (from Attacker VM)
- **Fast Scan** (top ports): runs quickly to find open ports
- **Service Version Detection + Default Script Scan**: identify services, versions, and run default NSE scripts for basic info

### 3. Document Findings
- Create a short report with:
  - Lab setup (OS, network mode)
  - Exact Nmap commands you ran
  - Top 3 interesting findings
  - One security recommendation for the target based on findings

---

## Deliverables (place these in `level2-vm-nmap/<your-github-handle>/`)
1. `report.md` — brief description of your VM setup, the exact Nmap commands used, top 3 findings, and one recommendation for hardening the target.  
2. `fast_scan.txt` — full, unedited output from the Fast Scan.  
3. `service_scan.txt` — full, unedited output from the Service/Script Scan.  
4. `screenshots/` — images showing both VMs running. Include at least:
   - `screenshots/vms_running.png` (or `.jpg`)
   - Any screenshot that contains output — but **redact** IPs/personal info.

> **CRITICAL:** Redact any public IP addresses, usernames, MAC addresses, or otherwise personal information from your report and screenshots **before** making the repo public or opening a PR.

---

## Suggested Folder Structure

level2-vm-nmap/  
└── <your-github-handle>/  
├── README.md  
├── report.md  
├── fast_scan.txt  
├── service_scan.txt  
└── screenshots/  
  └── vms_running.png  
---

## Example Nmap Commands (copy/paste — replace `<TARGET_IP>`)
> Use these exact commands on the **Attacker VM**. Save outputs to the files above.

**Fast Scan (top ports) — save output to `fast_scan.txt`:**
```bash
nmap -F -oN fast_scan.txt <TARGET_IP>
```

## What to include in report.md

Lab Setup: Attacker OS, Target OS, Virtualization software, Network mode (Host-Only/NAT)

Commands Run: exact commands (copy/paste from above, with <TARGET_IP> redacted if necessary)

Top 3 Findings: short bullets (e.g., “Open SSH (22) — OpenSSH 7.6p1; possible outdated version”, “HTTP (80) — Apache 2.4.29 with directory listing enabled”, “SMB anonymous share accessible”)

Recommendation: one concrete action (e.g., “Update OpenSSH to latest distro package and disable password auth; enable key-based auth only.”)
____________________

## Quick Redaction Checklist (don’t forget)

Replace actual IPs with <TARGET_IP> or REDACTED_IP in screenshots and report.md.

Blur or crop any images showing MAC addresses, cloud instance IDs, or usernames.

Remove any private keys or credentials from outputs.
____________________

## Submission

Place all deliverables into level2-vm-nmap/<your-github-handle>/.

Open a Pull Request as described in CONTRIBUTING.md.

____________________
