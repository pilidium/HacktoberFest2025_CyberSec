# Cybersecurity Hacktoberfest Repo

---

## Flow
Level 1 → Level 2 → Level 3 → Level 4  
Solo → Solo → Crowd-submissions → Team red vs blue

---

## Levels (short)
- **Level 1 — Foundations (Packet Tracer)**  
  Build a 2-PC + switch + router LAN, assign static IPs, ping, save `.pkt`, add `README.md`.

- **Level 2 — VM Lab & Nmap**  
  Two VMs (client + target), host-only/NAT, run `nmap -T4 -F` and `nmap -sV -sC`, submit outputs + report.

- **Level 3 — Crowd Wireshark Lab**  
  Each contributor: one client↔server interaction, one CSV row + `analysis.md` + PCAP/screenshots. Maintainers aggregate.

- **Level 4 — Red vs Blue Simulation**  
  Team-based. Weak-site in lab. Reds: recon + PCAPs. Blues: hardening + detection + incident report. Legal attestation required.

---

## Repo layout  
README.md  
CONTRIBUTING.md  
ISSUE_TEMPLATES/  
level1-foundations/  
level2-vm-nmap/  
level3/  
├─ submissions/  
└─ aggregated/  
level4/  
├─ weak-sites/  
└─ submissions/  

---

## How to contribute (2 steps)
1. Fork → branch `levelX/<yourhandle>/<task>` → add files under `levelX-.../<yourhandle>/`.  
2. Open PR titled `Level-X: <task> — <yourhandle>` and paste the level PR template into the description.

---

## Must-have rules
- **Lab-only**: only test on VMs or org-approved sandboxes.  
- **Redact** real IPs/MACs/keys.  
- **No exploit code** in repo.  
- Level-4 PRs **must** include `legal-ethics.md` ack.

---

## Templates available
Each level has copy-paste templates: report, PR template, submission CSV, analysis guide, legal-ethics text.

---

## Maintainers (quick)
- Use labels: `level-1`, `level-2`, `level-3`, `level-4`, `pcap`, `review-needed`.  
- Require 1 peer review for Level 3+ before merge.

---

## Quick grading rubric (single line)
Completeness · Clarity · Correctness · Ethics · Insight

---
