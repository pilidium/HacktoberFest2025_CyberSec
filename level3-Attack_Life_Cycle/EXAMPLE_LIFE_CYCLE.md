# Level 3 — FileCrypt Example (Metadata Tampering)

**Author:** Srimanthl2k6
Repo: [GitHub](https://github.com/Srimanthl2k6/Level-3-Example/tree/main) | [Video](https://www.youtube.com/watch?v=h_ROTfXwC3M&feature=youtu.be)

This example shows how **FileCrypt** secures file contents but trusts metadata (`files.db.json`), enabling a **Data Availability Attack** where tampering deletes/reassigns files. An exploit (`FileStealer`) demonstrates this flaw, and a patch uses **digital signatures** with unique file IDs to secure metadata. See `lifecycle_report.md` and the project report PDF for full lifecycle details. 
