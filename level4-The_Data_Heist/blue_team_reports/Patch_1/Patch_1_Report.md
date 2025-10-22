# Patch Report

**Date:** 23nd October 2025  
**Target:** Innovatech File Viewer  

---

## Vulnerability

The app was taking user input directly and using it to open files without checking if the filename's format was correct/safe.

**Problem:** Users could just type `../` to go back to parent folders and read ANY file on the server :O, not just files in the `files` folder.

**Example:**
- Normal: `welcome.txt` → reads `/files/welcome.txt` (like a normal sweet hooman would)
- Attack: `../secret_data.txt` → reads `/secret_data.txt` (like some bish ahh cunning hoomans would)

This Shouldn't Happen!! fk cunning hoomans

---

## The Patch

check if ".." is present in the given filename.

```python
if ".." in filename:
    error = "Invalid filename"
```

This stops users from using `../` to go to parent directories.

---

**The vulnerability is now fixed! YAYYY**