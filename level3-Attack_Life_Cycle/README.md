# Level 3: Attack & Defense Lifecycle Analysis (Collaborative)

## Objective
This is the first collaborative challenge. Each participant will document a full attack-and-defense lifecycle on a simple application. Your individual submission will then be aggregated with others to build a community knowledge base of vulnerabilities, exploits, and mitigation techniques.

## Refer to EXAMPLE_LIFE_CYCLE for better understanding

---

## ⚠️ Critical Security Warning
You are now working in a section of the repository that may contain executable files and proof-of-concept exploit code from other participants.  

- **DO NOT** run any code, scripts, or executables from other submissions unless you are in a completely isolated, sandboxed virtual machine that you are willing to have compromised.  
- **VERIFY ALL CODE YOURSELF.**  
- By participating, you acknowledge that you are responsible for your own safety and that you will not hold the project maintainers liable for any damage caused by running code from this repository.  
- All of your own activity **MUST** be strictly confined to your personal, isolated lab environment.  

---

## Your Task
Your goal is to create and document **one complete attack lifecycle**.

### 1. Find or Create a Vulnerable Application
- Write your own simple, vulnerable application (e.g., a Python script with a command injection flaw, a PHP site with an SQL injection vulnerability).  
**OR**  
- Use a well-known, publicly available vulnerable application (e.g., DVWA, Metasploitable services) inside a VM.  

### 2. Analyze and Exploit the Vulnerability
- Identify a specific weakness in the application.  
- Develop or use a script/method to exploit this weakness.  
- Document every step of the process.  

### 3. Patch and Remediate
- Modify the application's code to fix the vulnerability.  
- Verify that your patch successfully prevents the exploit from working.  

### 4. Submit Your Lifecycle
Create a pull request with a new folder containing all parts of your lifecycle analysis.  

---

## Required Submission Structure
Create a new folder:
level3/submissions/<your-github-handle>/  

Inside this folder, include the following:

- **`lifecycle_report.md`**  
  Your main report file. This should detail the entire process: the application, the vulnerability, the exploit steps, and the patch.  

- **`vulnerable_code/`**  
  A folder containing the source code and/or compiled binary of the application *before* you patched it.  

- **`exploit/`**  
  A folder containing any files used for the exploit. This can include scripts (`.py`, `.sh`), compiled executables (`.exe`), or other necessary files.  

- **`patched_code/`**  
  A folder containing the source code and/or compiled binary of the application *after* you fixed the vulnerability.  

---

## Collaborative Goal
The project maintainers will review all submissions.  
High-quality, well-documented lifecycles will be aggregated into a central database, creating a **shared resource** for learning about different attack vectors and defense strategies.
