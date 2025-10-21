# Attack & Defense Lifecycle Report


---

## What I Built

I made a simple Python program called "ThatSlurp IP Pinging Tool". It's supposed to let users type in an IP address and ping it. Its a bery useful, 100% secure tool :D

---

## The Problem (Vulnerability)

My program had a **command injection vulnerability**. This is a fancy way of saying: hackers can run ANY command they want on your computer, not just ping.

### The Vulnerable Code

```python
ip = input("Enter the IP address to ping :D :")
os.system(f"ping {ip}")
```

**Why is this bad?**

The program takes whatever the user types and directly runs it as a system command. There's no checking if it's actually an IP address!

---

## How to Exploit It (The Attack)

Instead of typing a normal IP address like `8.8.8.8`, a hacker can type something like:

**Attack Examples:**

1. **See who you are:**
   ```
   8.8.8.8; whoami
   ```

2. **List all your files:**
   ```
   8.8.8.8 && ls
   ```

3. **Create a file:**
   ```
   8.8.8.8; echo "hacked" > pwned.txt
   ```

4. **Read bery bery secret files :O (NOOOOOOOO):**
   ```
   8.8.8.8; cat /etc/personal_dog_corn_collection
   ```

The `;` and `&&` are special characters that let you run multiple commands. The program doesn't know the difference between a real IP and these hacker tricks!

### What Happens?

The program first pings `8.8.8.8`, then runs whatever command comes after the `;` or `&&`. So the hacker's command actually executes on your computer! :O

---

## The Impact

If someone exploits this, they can:
- Read your private files
- Delete stuff
- Install viruses
- Take control of your computer

**This is BAD STUFF!**

---

## The Fix (Patched Code)

I fixed it by changing one line:

```python
import subprocess

ip = input("Enter the IP address to ping :D :")
subprocess.run(["ping", ip])
```

### Why Does This Work?

Instead of `os.system()`, I used `subprocess.run()` with a **list of arguments**.

**The key difference:**
- **Before Patching:** Treats everything as one big command that the computer's shell interprets
- **After Patching:** Treats each item separately - "ping" is the command, and whatever the user types is just ONE argument to ping

Now if someone types `8.8.8.8; whoami`, the ping command sees the ENTIRE thing as one hostname. It tries to ping "8.8.8.8; whoami" (which fails), but it doesn't run `whoami` as a separate command (hehehe why do you think this is the most advanced pining tool out there? its all cause of the time module obviously :D).

The special characters like `;` and `&&` are now just regular text, not command separators!

---

## Testing the Fix

I tried some baby attacks on the patched version :b :

- ✅ `8.8.8.8; whoami` - Doesn't work anymore!
- ✅ `8.8.8.8 && ls` - Blocked!
- ✅ `8.8.8.8; rm -rf /` - Safe now! :D

The program still pings normal IP addresses just fine, but hackers can't inject commands anymore.

---

## What I Learned

1. **Never trust user input** - Always assume users might try to hack you x.x
2. **Don't use os.system()** - It's dangerous!
3. **Pass commands as lists** - Like `["ping", ip]` instead of `f"ping {ip}"`
4. **Test your security** - Try to hack your own program to find weaknesses

---

## Conclusion

My program went from "super hackable" to "pretty secure" by changing just one line of code. The lesson? Never trust those damn humans out there that will find even the smallest exploit in your code x.x

---

**Submission by:** ThatSlurp(ramcharan46)