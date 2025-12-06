```markdown
<p align="center">
  <!-- Replace this link after uploading your banner -->
  <img src="banner.png" alt="Cyber Automation Pro Banner" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CYBER%20AUTOMATION%20PRO-v1.0-black?style=for-the-badge&logo=linux&logoColor=green">
  <img src="https://img.shields.io/badge/STATUS-STABLE-green?style=for-the-badge&logo=check-circle">
  <img src="https://img.shields.io/badge/PLATFORM-Kali%20|%20Ubuntu%20|%20WSL-red?style=for-the-badge&logo=kalilinux">
  <img src="https://img.shields.io/badge/LICENSE-MIT-blue?style=for-the-badge&logo=mit">
  <img src="https://img.shields.io/badge/USAGE-Red%20Team%20|%20Bug%20Bounty-yellow?style=for-the-badge&logo=bug">
  <img src="https://img.shields.io/badge/Python-3.10%2B-blueviolet?style=for-the-badge&logo=python">
</p>

---

```
    ____      _               ___        _        _   _             _             
   / ___|   _| |__   ___ _ __|_ _| _ __ | |_ __ _| |_(_) ___  _ __ (_)_ __   __ _ 
  | |  | | | | '_ \ / _ \ '__|| | | '_ \| __/ _` | __| |/ _ \| '_ \| | '_ \ / _` |
  | |__| |_| | |_) |  __/ |   | | | | | | || (_| | |_| | (_) | | | | | | | | (_| |
   \____\__,_|_.__/ \___|_|  |___||_| |_|\__\__,_|\__|_|\___/|_| |_|_|_| |_|\__, |
                                                                            |___/ 
                  CYBER AUTOMATION PRO v1.0 — SKULL HACKER EDITION [December 2025]
```

> **Automated Red-Team Recon • Local Network Mapping • Bug Bounty Scanner • CVE Hints → Executive Reports • Telegram Alerts**

---

# ⚔ CYBER AUTOMATION PRO v1.0

## Automated Pentest & Bug Bounty Recon Framework

**Release Date:** December 05, 2025  
**Author:** Hemanth Karal Varmaa (0xDEADVrm) [web:45]

> *"The future belongs to those who automate offense."* — 0xDEADVrm 😈🔥

---

## 🧩 **Core Features**

| Feature | Description |
|---------|-------------|
| **🌐 Local Network Scanner** | Nmap-based CIDR scanning with service/version detection → CSV export [web:17] |
| **🎯 Bug Bounty Recon** | Subdomain enumeration + HTTP/HTTPS liveness probe + title extraction |
| **🕵️ Vulnerability Hints** | Port/service → common attack surface mapping (FTP/SSH/Web/DB/RDP) |
| **📄 Auto Reports** | Professional DOCX with summary tables + raw CSV paths |
| **📲 Telegram Alerts** | Optional instant notifications with report links |
| **🔄 Cron Ready** | Filesystem layout optimized for scheduled automation |

---

## 🧱 **Project Structure**

```
cyber-automation-pro/
│
├── main.py                 # Orchestrator
├── config.json            # Central configuration
├── requirements.txt       # Python dependencies
├── subdomains.txt         # Bug bounty wordlist
│
├── modules/
│   ├── local_scan.py      # Nmap local network scanner
│   ├── bounty_scan.py     # Subdomain + HTTP probing
│   ├── vuln_lookup.py     # Heuristic vulnerability suggestions
│   ├── report_gen.py      # DOCX report generator
│   └── notify.py          # Telegram notifications
│
├── output/
│   ├── reports/           # Generated DOCX files
│   └── raw/               # CSV scan data
└── logs/                  # Cron/Task Scheduler logs
```

---

## 📦 **Quick Installation**

### 1. Clone & Setup

```
git clone https://github.com/YOUR_USERNAME/cyber-automation-pro.git
cd cyber-automation-pro
```

### 2. Python Environment

```
python3 -m venv venv
source venv/bin/activate  # Linux/macOS
# .\venv\Scripts\activate  # Windows

pip install -r requirements.txt
```

**requirements.txt:**
```
python-nmap
requests
python-docx
pandas
```

### 3. System Dependencies

**Kali/Ubuntu/WSL:**
```
sudo apt update && sudo apt install nmap
```

**Windows:** Install Nmap and add to PATH [web:10]

---

## ⚙ **Configuration** (`config.json`)

```
{
  "local_scan": {
    "enabled": true,
    "target_cidr": "192.168.1.0/24",
    "nmap_args": "-sC -sV -O"
  },
  "bug_bounty": {
    "enabled": true,
    "root_domain": "example.com",
    "subdomain_wordlist": "subdomains.txt",
    "http_timeout": 5
  },
  "report": {
    "output_dir": "output/reports",
    "include_raw_data": true
  },
  "notification": {
    "telegram": {
      "enabled": false,
      "bot_token": "YOUR_BOT_TOKEN",
      "chat_id": "YOUR_CHAT_ID"
    }
  }
}
```

---

## 🚀 **Usage**

### 1. Create `subdomains.txt`
```
www api admin dev test staging portal vpn mail support dashboard login app
```

### 2. Run Full Scan
```
python3 main.py
```

**Output:**
```
[+] Scanning local network: 192.168.1.0/24 with args: -sC -sV -O
[+] Local scan results saved to output/raw/local_scan_20251206_231200.csv
[+] Bug bounty scan for: example.com
[+] Alive: https://www.example.com 
[+] Bug bounty scan results saved to output/raw/bounty_scan_20251206_231205.csv
[+] Report saved to output/reports/report_20251206_231210.docx
[+] Telegram notification sent.
```

---

## 📊 **Sample Report Structure**

**Generated DOCX contains:**
1. **Executive Summary** - Host counts, findings overview
2. **Local Network Services** - Top 50 (IP/Port/Service/Version)
3. **Bug Bounty Targets** - Alive subdomains (URL/Status/Title)
4. **Vulnerability Suggestions** - Prioritized testing areas
5. **Raw Data Links** - CSV paths for analysis

---

## 🔄 **Automation Setup**

### **Cron (Linux/Kali/WSL)**
```
crontab -e
```
```
0 2 * * * cd /path/to/cyber-automation-pro && /usr/bin/python3 main.py >> logs/cron.log 2>&1
```
```
mkdir -p logs output/{reports,raw}
```

### **Windows Task Scheduler + WSL**
```
Program: wsl.exe
Arguments: python3 /mnt/c/path/to/cyber-automation-pro/main.py
```

---

## 🧠 **Module Breakdown**

| Module | Purpose | Output |
|--------|---------|--------|
| `local_scan.py` | Nmap CIDR scan | CSV with IP/ports/services [web:1] |
| `bounty_scan.py` | Subdomain → HTTP probe | CSV with alive URLs/status |
| `vuln_lookup.py` | Port/service → attack hints | Prioritized testing list |
| `report_gen.py` | Data → DOCX report | Professional Word document |
| `notify.py` | Report → Telegram | Instant mobile alerts |

---

## 🗺 **Roadmap**

### **v1.x (Immediate)**
- [ ] JSON/HTML report formats
- [ ] Error handling + retry logic
- [ ] Config validation

### **v2.0 (Q1 2026)**
- [ ] Vulners API integration [web:34]
- [ ] Nikto/WhatWeb automation [web:8]
- [ ] Metasploit RPC modules [web:23]
- [ ] Risk scoring + CVSS charts
- [ ] Web dashboard

---

## 👤 **Author**

**Hemanth Karal Varmaa**  
*aka 0xDEADVrm*  
**Cybersecurity Researcher | Bug Bounty Hunter | Red Teamer**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/varmaa07)

---

## ⭐ **Support the Project**

If Cyber Automation Pro saves you time:

- ⭐ **Star** the repository
- 🐛 **Report** bugs via Issues
- 🔧 **Contribute** via Pull Requests
- 📢 **Share** with your cybersecurity community

**Feature Requests Welcome:** AI analysis, C2 integration, auto-exploitation [web:40]

---

## ⚖ **Legal & Ethical Notice**

```
🔴 THIS TOOL IS FOR:
✅ Authorized penetration testing
✅ Red team engagements  
✅ Bug bounty programs (with permission)
✅ Educational/research purposes

❌ NEVER USE ON:
❌ Systems without explicit permission
❌ Production environments without authorization
❌ Third-party infrastructure
```

**Author not liable for misuse.** Always follow responsible disclosure [web:52]

---

```
---------------------[ Crafted with ⚔💀 by 0xDEADVrm | Dec 2025 ]---------------------
```
