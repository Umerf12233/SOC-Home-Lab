# 🛡️ SOC Home Lab — Real Attack Detection

> Practical cybersecurity home lab simulating real attacks and detecting them using enterprise-grade SIEM tools.

## 👨‍💻 Analyst
**Name:** [Your Name]  
**Role:** SOC Analyst L1  
**Location:** Pakistan  

---

## 🔧 Lab Setup
| Component | Tool | Purpose |
|-----------|------|---------|
| SIEM | Wazuh 4.x | Real-time threat detection |
| Attacker Machine | Kali Linux | Attack simulation |
| Virtualization | VirtualBox | Isolated lab environment |
| Network | 192.168.100.0/24 | Internal only |

---

## ⚔️ Attacks Simulated & Detected

### IR-2026-001 — Trojaned Binary Detection
- **Attack:** `/usr/bin/chsh` replaced with trojaned version
- **Detection:** Wazuh rootcheck — Rule ID 510
- **Severity:** Medium (Level 7)
- **MITRE:** T1036 (Masquerading) | T1548 (SUID Abuse)
- 📄 [IR Report](./IR_Report_2026_001_Trojaned_Binary.docx)

### IR-2026-002 — SSH Brute Force Attack
- **Attack:** Hydra + rockyou.txt — 14M password attempts
- **Detection:** Wazuh PAM logs — Rule ID 5503 | 1,035+ alerts
- **Severity:** High (Level 10)
- **MITRE:** T1110.001 (Password Guessing)
- 📄 [IR Report](./IR_Report_2026_002_SSH_BruteForce.docx)

---

## 📊 Alert Statistics
| Attack | Before | After | Spike |
|--------|--------|-------|-------|
| Trojaned Binary | 0 | 229 hits | ✅ Detected |
| SSH Brute Force | 28 Medium | 184 Medium + 1,035 Low | 🔴 Massive Spike |

---

## 🗺️ MITRE ATT&CK Coverage
- T1046 — Network Service Discovery
- T1036 — Masquerading
- T1548.001 — SUID Abuse
- T1110.001 — Password Guessing
- T1543 — Persistence via Modified Binary

---

## 🛠️ Tools Used
`Wazuh` `Kali Linux` `Hydra` `Nmap` `VirtualBox` `MITRE ATT&CK`

---

## 📬 Connect
[LinkedIn](your-linkedin-url) | [GitHub](https://github.com/Umerf12233)
