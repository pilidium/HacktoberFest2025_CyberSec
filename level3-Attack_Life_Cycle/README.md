# Level 3: Attack Lifecycle — Vulnerability → Exploit → Patch → Document

**Goal:** Build and document a full attack lifecycle for a small app: demonstrate the vulnerability, show the (conceptual) attack, patch the app, and validate the fix. Submit source, sanitized artifacts, and structured metadata for ingestion into the course database.

> Safety-first: public repos must NOT contain runnable exploit binaries or other hazardous payloads. Use private instructor channels for any sensitive binaries.

---

## What you must submit (place in `level3-life-cycles/<your-github-handle>/`)
- `report.md` — lifecycle writeup (template below).
- `vulnerable_source/` — source code of the vulnerable app (no compiled binaries).
- `patch_source/` — patched source or unified diff (`git diff` or patch file).
- `attack_demo.txt` — high-level steps or pseudocode showing the attack concept (non-executable).
- `artifacts/` — screenshots, logs, diffs (images, txt, but NO binaries).
- `metadata.json` — structured metadata for the central DB (schema below).

**Optional (instructor-only):**
- If grading requires binaries, upload them to the private instructor bucket and document the path in `report.md` (see CONTRIBUTING for how).

---

## Minimal `report.md` (required fields)
- One-line summary (attack → impact → patch)
- Environment (OS, runtime, isolation)
- Vulnerability (type, location in code, impact)
- Attack (high-level; **no runnable exploit code**)
- Patch (what changed, why it fixes)
- Validation (how you tested)
- Artifacts list (images, diffs)
- Private artifacts note (if applicable)

_A `report.md` template is provided in the repo._

---

## Safety rules (must follow)
- **Do NOT** commit `.exe`, `.dll`, `.bin`, `.apk`, `.msi`, `.so` or other executables to the **public** repo.
- Source code is OK (vulnerable & patched).
- Screenshots/logs must be redacted of public IPs, cloud IDs, and credentials.
- `metadata.json` must include `"exploit_public": false` if exploit files exist privately.

---

## Submission flow
1. Create branch `level3/<your-handle>`.
2. Add your folder `level3-life-cycles/<your-handle>/` with required files.
3. Open PR using the Level 3 PR template.
4. If you have private binaries for instructors, request private upload per CONTRIBUTING instructions.

---

## Instructor notes
- A GitHub Action blocks any PR containing forbidden binary extensions.
- Instructors may request private artifacts via secure bucket; the PR must reference the private location and the repo must set `"exploit_public": false`.
---

## report.md template (paste into each student folder)

# Project: <short name>

> This example is intentionally minimal — just a basic idea. Use any tools (including AI), frameworks, or languages you like. The goal is to produce useful information and insights about an attack → defense → patch lifecycle.

---

## 1. Attack (details)
- **Summary:** One-sentence description of the attack.  
- **Target / Trigger:** Which component or input is vulnerable? (file, endpoint, function)  
- **Steps (high-level):** Describe the attack flow step by step. Keep this conceptual — do **not** include runnable exploit binaries or full exploit payloads in the public repo.  
  1. ...
  2. ...
- **Impact:** What did the attack achieve? (confidentiality / integrity / availability / data exfiltration / privilege escalation / etc.)

---

## 2. Defense (detection & mitigation)
- **How it was detected:** Logs, manual inspection, monitoring, fuzzing, static analysis, etc.  
- **Immediate mitigations:** Quick actions taken to reduce risk (config, disable service, network isolation).  
- **Longer-term defenses:** Design changes, validation, authentication, access controls, monitoring, or other controls that stop or detect the attack.

---

## 3. Patch (what was changed)
- **Files changed / diff:** (point to `patch_source/` or list filenames)  
- **Patch summary (short):** Explain the exact fix (e.g., added input validation + canonicalize paths; replaced unsafe write with atomic write; enforced auth).  
- **Why the patch works:** Brief justification of why this prevents the attack.  
- **Verification:** How you tested the patch (manual steps, unit tests, logs). Results: pass / fail / notes.

---

## 4. Screenshots (embedded)
Place screenshots in `artifacts/` inside your submission folder and keep filenames exact so they render.

**VMs / lab view:**  
![VMs Running](artifacts/vms_running.png)

**Attack / detection / test output:**  
![Demo Output](artifacts/demo_output.png)

> **Redaction reminder:** Before making public, redact any public IPs, credentials, keys, hostnames, cloud IDs, or other sensitive data in screenshots and logs.

---

## Final note
This example is only a minimal guide. Use **any tools** (including AI) and any workflow you prefer. What matters is the value of the final submission: clear descriptions, evidence (screenshots/logs/diffs), and actionable insights about how the vulnerability was exploited and fixed.
