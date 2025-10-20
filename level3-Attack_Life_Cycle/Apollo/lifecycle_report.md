Damn Vulnerable Web Application (DVWA) is a web application default to Metasploitable services. It acts as a database and stores harmless data. This web application functions as a target dummy for amateur cybersecurity students to practice attacks and make applications more robust to prevent the same attacks.

---

### ✨ Features

* 🔐 **Secure User Access:** The system is set in a virtual lab network that is local to your device. Since the network is not connected to the internet, it provides a safe lab to test attacks.
* 💾 **Persistent Storage:** User accounts and encrypted files are saved locally and persist between application sessions.
* 👨‍💻 **User-Controlled:** The device user has complete access to both the Virtual Machines, making it extremely flexible for any sort of testing.

---

### 🚀 Usage

1.  Install Metasploitable 2 and Kali Linux (Metasploitable is the service we are going to exploit using Kali Linux)
2.  Set them up in an isolated lab environment (preferably an internal network) with assigned static IPs. The process to assign static IPs is given in this [Google Docs](https://docs.google.com/document/d/1NSHCtkjq4dB2hhEdRLRD8jMFoLfQ4ichKgnPBOIIvgE/edit?usp=sharing)
3.  In your Kali Linux browser, enter ```http://<metasploitable-ip>/dvwa/```
4.  In the DVWA login that appears, use the `admin`/`password` credentials to log into the UI.
5.  Go to the setup page from the options displayed on the left and click **Create/Reset Database**. This creates a new databse for your testing.
6.  Go to DVWA Security and set it to **Low**.
7.  Head over to the Command Execution section and enter ```<metasploitable-ip>; echo test``` in the box.
8.  As shown in the attached image, if the command is executed, the phrase text is printed at the bottom.
9.  Experiment in similar fashion with **Medium** and **High** security levels. The results for them are attached as well.

---

### 🔬 Project Demonstration: Vulnerability & Patch

This project a critical security flaw and its solution, forming a complete development lifecycle.

#### The Vulnerability: Data Availability Attack

> The initial version of the Damn Vulnerable Web Application (DVWA) has security set to Low. This causes the application's database to be unencrypted, making the data vulnerable to breaches.

* **The Exploit:** An attacker VM (Kali Linux) was used to demonstrate the flaw. This tool was used to access the DVWA through the internal network. By using Command Injection, the attacker VM could gain access to the web application's database and modify it.

* **The Impact:** This resulted in a data breach. When the victim logged back into DVWA, their database was reset, making the data permanently inaccessible.

#### The Proposed Fix: Increased Security Checks and Firewalls

> To make the application invulnerable to this type of tampering, the user's IP must have permissions to access the file.

* **The Solution:** The patched version of the application would have higher security measures that log the user's IP and make sure it has permissions to access the file. If permissions are not availed to the user, their access to the database is denied. The firewall also prevents other users from accessing the database unauthorized.

---
