## Level 2: VM Lab & Nmap Scan

**Task:**  
Set up two VMs on a private virtual network (attacker + target). From the attacker VM, run two Nmap scans against the target and submit a short report, the raw outputs, and screenshots.

## Required files (place in `level2-vm-nmap/<your-github-handle>/`)
- `report.md` — brief report (see template below)
- `fast_scan.txt` — output of `nmap -F`
- `service_scan.txt` — output of `nmap -sV -sC`
- `screenshots/vms_running.png` — screenshot showing both VMs running
- `screenshots/nmap_output.png` — screenshot of the attacker terminal with Nmap output

## Nmap commands to run (from attacker VM)
```bash
nmap -F <TARGET_IP>               # fast scan (top ports)
nmap -sV -sC <TARGET_IP>          # service/version detection + default scripts
```
## Level 2 Submission: Nmap Scan Report

## 1. Lab Environment Setup
Attacker: OS: ______, Network Mode: ______, IP: `REDACTED`  
Target: OS: ______, Network Mode: ______, IP: `REDACTED`

## 2. Nmap Commands Executed
```bash
nmap -F <TARGET_IP>
nmap -sV -sC <TARGET_IP>
```
# 3. Findings

Port 21/tcp: ______

Port 23/tcp: ______

Port 80/tcp: ______
