# Level 2: VM Lab & Nmap Scan

**Task:**  
Set up two VMs on a private virtual network (attacker + target). From the attacker VM, run two Nmap scans against the target and submit a short report, the raw outputs, and screenshots.

---

## Required files (place in `level2-vm-nmap/<your-github-handle>/`)
- `report.md` — brief report (includes top 3 findings **and one security recommendation**)
- `fast_scan.txt` — output of `nmap -F -oN fast_scan.txt <TARGET_IP>`
- `service_scan.txt` — output of `nmap -sV -sC -oN service_scan.txt <TARGET_IP>`
- `screenshots/vms_running.png` — screenshot showing both VMs running
- `screenshots/nmap_output.png` — screenshot of the attacker terminal with Nmap output

**Important:** `report.md` **must** include these exact lines so images render on GitHub:

```markdown
![VMs Running](screenshots/vms_running.png)
![Nmap Output](screenshots/nmap_output.png)
```
Before you make the repo public or open a PR, redact any public IPs, usernames, private keys, MACs, or cloud instance IDs.
```bash
nmap -F -oN fast_scan.txt <TARGET_IP>            # fast scan (top ports)
nmap -sV -sC -oN service_scan.txt <TARGET_IP>    # service/version detection + default scripts
```
Move fast_scan.txt and service_scan.txt into your submission folder.
____________________

## Minimal report.md template (paste into report.md and fill in)

# Level 2 Submission: Nmap Scan Report

## 1. Lab Environment Setup
Attacker: OS: ______, Network Mode: ______, IP: `REDACTED`  
Target: OS: ______, Network Mode: ______, IP: `REDACTED`

## 2. Nmap Commands Executed
```bash
nmap -F -oN fast_scan.txt <TARGET_IP>
nmap -sV -sC -oN service_scan.txt <TARGET_IP>
```
# 3. Findings (top 3)

Port 21/tcp: ______

Port 23/tcp: ______

Port 80/tcp: ______

# 4. Recommendation (one action)

______ (e.g., disable telnet, enable SSH with key auth, update/remove vulnerable service)

# 5. Screenshots (embedded)

---
