# Patch Report

**Date:** 24th October 2025  
**Target:** Innovatech File Viewer  

---

## Vulnerability

The `secret_data.txt` file was stored in plain text in the repository, so anyone with access to the files could read it directly.

**Problem:** Attackers could create Python scripts in the repo that open and read `secret_data.txt` directly :O

**Example:**
- Normal: Use the web app to view files (like a normal sweet hooman would)
- Attack: Write a Python script that does `open('secret_data.txt').read()` and steal the data (like some bish ahh cunning hoomans would)

This Shouldn't Happen!! fk cunning hoomans

---

## The Patch

Encrypt the `secret_data.txt` file so it can't be read without the decryption key.

```python
def encrypt(text, key):
    return ''.join(chr(ord(c) ^ ord(key[i % len(key)])) for i, c in enumerate(text))

def decrypt(text, key):
    return ''.join(chr(ord(c) ^ ord(key[i % len(key)])) for i, c in enumerate(text))

KEY="secret123" #this is not the key i used obv :D
decrypted_data=decrypt(encrypte_content, KEY)
```

This encrypts the secret data. Even if attackers get the encrypted file, they can't read it without the KEY (which is NOT in the repo) hehehehe fk u charan.

---

**The vulnerability is now fixed! YAYYY**