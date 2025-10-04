# 🕵️‍♂️ Level 4: Live Red vs. Blue – The Data Heist

Welcome to the **final challenge** — a live, team-based, competitive exercise where:

- 🔴 **Red Team's Goal**: Steal the secret file.
- 🔵 **Blue Team's Goal**: Stop the Red Team by patching vulnerabilities.

This simulation is managed by automated workflows that announce turns and enforce time limits.

---

## 🧠 The Battlefield

The heart of this challenge is a **vulnerable application** located in:
level4/vulnerable-app/

Hidden within this app is a file named:
secret_data.txt

---

## 🎯 Objectives

### 🔴 Red Team (Attackers)
- **Goal**: Exploit a vulnerability to read `secret_data.txt`.
- **Deliverable**: A report proving the successful theft.

### 🔵 Blue Team (Defenders)
- **Goal**: Patch the exploited vulnerability to prevent future theft.
- **Deliverable**: A code update that secures the application.

---

## 🔁 The Game Loop

1. **Red Team Steals the File**  
   Analyze the latest version, find an exploit, and submit a Pull Request with proof.

2. **Blue Team Patches the Flaw**  
   Once the Red Team's PR is merged, the Blue Team must submit a patch via PR.

3. **Cycle Repeats**  
   After the patch is merged, the Red Team must find a new way in.

---

## 🕹️ How to Play

- **Join a Team**:  
  Go to the **Issues** tab and open a new issue using the  
  `Level 4: Join the Simulation` template.

- **Coordinate in Your Forum**:  
  Each team gets a dedicated `Strategy` issue to plan and discuss.

- **Take a Turn**:  
  One team member opens a Pull Request with the team's action.

- **Meet the Deadline**:  
  Each team has **48 hours** to submit their PR once their turn begins.

---

## 📦 Team Deliverables

### 🔴 Red Team Report

- 📁 Location: `level4/red-team-reports/`
- 📄 Contents:
  - Detailed explanation of the vulnerability and exploit steps.
  - Exact contents of `secret_data.txt` as proof.
  - Link to a video (e.g., YouTube, Loom) showing the attack in action.

### 🔵 Blue Team Patch

- 📁 Location: `level4/vulnerable-app/`
- 📄 PR Description:
  - Patch notes explaining what was changed and why.
  - Link to a video walkthrough of the vulnerability and the fix.

---

## 🏆 Winning Conditions

- ✅ **Red Team Wins** if the Blue Team fails to patch within 48 hours.
- ✅ **Blue Team Wins** if the Red Team fails to steal the file within 48 hours.

---

Let the battle begin! 💥
