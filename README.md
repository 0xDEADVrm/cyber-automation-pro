<p align="center">
  <img src="https://raw.githubusercontent.com/0xDEADVrm/cyber-automation-pro/main/banner.png" alt="Cyber Automation Pro Banner"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CYBER%20AUTOMATION%20PRO-v1.0-black?style=for-the-badge&logo=linux&logoColor=green">
  <img src="https://img.shields.io/badge/STATUS-STABLE-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/PLATFORM-KALI%20LINUX-red?style=for-the-badge&logo=kalilinux">
  <img src="https://img.shields.io/badge/LICENSE-OpenSource-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/TOOLS-Red%20Team%20|%20Bug%20Bounty-yellow?style=for-the-badge">
</p>

---

# ⚔ CYBER AUTOMATION PRO v1.0 — Skull Hacker Cyberpunk Edition
### **Automated Pentest & Bug Bounty Recon Framework**
**Release Date:** December 05, 2025  
Created By **0xDEADVrm**

> Automated Red-Team Recon | CVE → ExploitDB → AI Report | Telegram Alerts | Offensive Automation

---

## 🏆 Release Highlights
| Feature | Description |
|---------|-------------|
| ⚡ Automated Recon & Pentest Workflow | Scanning → CVE Detection → ExploitDB PoC Lookup → PDF/DOCX Report |
| 🧠 AI Risk Analysis | GPT-powered remediation + risk summary |
| 🌎 Bug Bounty Recon Engine | Subfinder, HTTPX, WhatWeb, optional Nikto |
| 🎯 Shodan Enrichment | Exposed service fingerprinting |
| 💣 ExploitDB PoC Lookup | Auto-search for public exploit PoCs |
| 🧾 Auto Reports | DOCX & PDF with charts and AI summary |
| 📲 Telegram Alerts | Instant notification with result files |
| 🔥 ASCII Cyberpunk UI | Animated terminal interface |

---

## 🛠 Fixes & Improvements
| Category | Improvement |
|----------|-------------|
| Nmap scanning | Faster runtime & CSV export |
| Vulners integration | Deprecation-safe handling |
| exploitdb_lookup module | CVE → Title & URL exploit match |
| Recon Module | HTTPS detection & CSV cleanup |
| Reporting Engine | Multi-format export |
| AI Module | Structured recommendations |
| Telegram | File + message delivery stable |

---

## 📦 Changelog

### **Added**
- `exploitdb_lookup.py` — Exploit retrieval engine
- `ai_risk.py` — Vulnerability scoring w/ GPT
- `charts_ascii.py` — ASCII CVSS chart generator
- PDF & DOCX dual output
- Telegram notifications

### **Updated**
- `main.py` — redesigned workflow
- `bounty_scan.py` — signature & CSV structure
- `report_gen.py` — AI summary integration
- `local_scan.py` — simplified model

### **Removed**
- Deprecated UI animation
- Web dashboard (moved to v2.0 roadmap)

---

## ⚠ Known Issues
| Issue | Status |
|--------|--------|
| Metasploit RPC auto-connect may fail | Start manually if msfrpcd is inactive |
| No CVE found = skip ExploitDB lookup | Intended behavior |

---

## ⚙ Requirements
- Python **3.10+**
- Kali Linux / Ubuntu recommended
- Dependencies: `nmap`, `subfinder`, `httpx`, `whatweb`, `nikto` (optional)

---

## 🔐 API Keys (config.json)
```json
{
  "openai.api_key": "",
  "shodan.api_key": "",
  "vulners.api_key": "",
  "telegram.bot_token": "",
  "telegram.chat_id": ""
}
