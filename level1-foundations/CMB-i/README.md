# SOHO Network – Static IP Configuration (192.168.1.0/24)

**Topology:**

<img width="774" height="242" alt="Screenshot 2025-10-22 at 12 30 45 AM" src="https://github.com/user-attachments/assets/441ce374-8b41-450e-8287-ec28950599f9" />

**Goal:** Both PCs should be able to ping each other successfully.

---

## IP Addressing Scheme

| Device | Interface | IPv4 Address | Subnet Mask | Default Gateway |
|:------:|:-----------|:-------------|:-------------|:----------------|
| Router | G0/0 | 192.168.1.1 | 255.255.255.0 | — |
| PC1 | FastEthernet0 | 192.168.1.10 | 255.255.255.0 | 192.168.1.1 |
| PC2 | FastEthernet0 | 192.168.1.11 | 255.255.255.0 | 192.168.1.1 |

---
## Ping verification

- from PC1 to PC2
  
  <img width="572" height="434" alt="image" src="https://github.com/user-attachments/assets/6ee6d5ea-4145-4a76-94b8-ec05d192c45f" />

- from PC2 to PC1

  <img width="578" height="440" alt="image" src="https://github.com/user-attachments/assets/0bfdeae4-944c-44ee-bd93-580bac5ff4f7" />
