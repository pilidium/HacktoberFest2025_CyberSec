# Patch Report

**Date:** 24th October 2025  
**Target:** Innovatech File Viewer  

---

## Vulnerability

The app was checking for `..` And absolute paths in filenames to prevent directory traversal, BUT it wasn't checking if the file was a symlink (symbolic link).

**Problem:** Users could create a symlink inside the `files/` folder that points to ANY file on the server :O, completely bypassing the `..` and absolute path check.

**Example:**
- Normal: `welcome.txt` → reads `/files/welcome.txt` (like a normal sweet hooman would)
- Attack: Create symlink `link.txt` → points to `../secret_data.txt` → reads `/secret_data.txt` (like some bish ahh cunning hoomans would)

This Shouldn't Happen!! fk cunning hoomans

---

## The Patch

check if the file is a symlink before reading it.

```python
if os.path.isfile(file_path) and not os.path.islink(file_path):
    with open(file_path, 'r') as f:
        content = f.read()
```

This stops users from using symlinks to access files outside the `files/` folder.

---

**The vulnerability is now fixed! YAYYY**