# Patch Report

**Date:** 24th October 2025  
**Target:** Innovatech File Viewer  

---

## Vulnerability

The app was taking user input directly and using it to open files without checking if the filename's format was correct/safe.

**Problem:** Users could bypass the `..` check by using absolute paths to read ANY file on the server :O, not just files in the `files` folder.

**Example:**
- Normal: `welcome.txt` → reads `/files/welcome.txt` (like a normal sweet hooman would)
- Attack: `C:/home/user/secret_data.txt` → reads `C:/home/user/secret_data.txt` (like some bish ahh cunning hoomans would)

This Shouldn't Happen!! fk cunning hoomans

---

## The Patch

Added check to reject absolute paths along with the existing `..` check.

```python
if (".." in filename) or os.path.isabs(filename):
    error = "Invalid filename."
```

This stops users from:
1. Using `../` to go to parent directories (already blocked)
2. Using full absolute paths like `/etc/passwd` or `C:\secret.txt` (NOW blocked)

---

**The vulnerability is now fixed! YAYYY**