**Date:** 24thd October 2025
**Target:** Innovatech File Viewer
**Vulnerability:** Symbolic Link (Symlink)

---

## 🕵️ Vulnerability Analysis
By creating a symlink to `secret_data.txt` and calling the symlink, I can view the contents of the file.

## 👨‍💻 Exploitation Steps

1. Open terminal and navigate to the directory
2. Run `mklink files\link.txt ..\secret_data.txt`. This creates a symlink that let's me access the data of `secret_data.txt`

## 📃 Proof of Compromise

Contents of `secret_data.txt` are - 
```
Loser checking the content through the repo 🤣🫵
bish ahh, Go attack the app 🤣🫵
```