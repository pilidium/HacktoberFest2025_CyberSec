**Date:** 23rd October 2025
**Target:** Innovatech File Viewer
**Vulnerability:** Unrestricted Path Traversal

---

## 🕵️ Vulnerability Analysis
The program does not ensure that the final path entered is in the `files` directory, making it easy to bypass by using the entire sequence to access the parent files.

## 👨‍💻 Exploitation Steps

### Method 1:
1. Run `app.py` to start the application
2. Open the application in the [localhost](http://127.0.0.1:8080)
3. Enter the full path of `secret_data.txt` as the filename
4. Click `View File`
5. Contents of `secret_data.txt` can be viewed

### Method 2: 
1. Run `app.py` to start the application
2. Attack the application with the following `http://127.0.0.1:8080/?filename=<full_path>/secret_data.txt`

A usual request would go like `http://127.0.0.1:8080/?filename=<file>`
By using the entire path of `secret_data.txt`, I am bypassing the check for `..`.

**P.S. -** Contents of `app.py` can be viewed in the same way as well.

## 📃 Proof of Compromise

Contents of `secret_data.txt` are - 
```
Loser checking the content through the repo 🤣🫵
U aint smart bozo, Go attack the app 🤣🫵
```