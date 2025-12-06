🚀 CYBER AUTOMATION PRO v1.0 — Skull Hacker Cyberpunk Edition
Automated Pentest & Bug Bounty Recon Framework

Released on: Dec 05, 2025

🏆 Highlights of This Release
Feature	Description
⚡ Automated Recon & Pentest Workflow	Full pipeline from scanning → CVE → ExploitDB → PDF report
🧠 AI Risk Analysis (GPT Powered)	Automated summarization & remediation guidance
🌎 Bug Bounty Recon Engine	Subfinder, HTTP probe, WhatWeb, Nikto (optional)
🎯 Shodan Enrichment	IP threat exposure lookup
💣 ExploitDB PoC Lookup	Auto search for public exploit PoCs
🧾 Auto Reports	Generate DOCX + PDF with charts & AI summary
📲 Telegram Alerts	Get scan results instantly on your phone
🔥 ASCII Cyberpunk UI	Animated terminal banners and progress spinners
🛠 Fixes & Improvements
Category	Description
Improved Nmap local scanning	Clean return structure & CSV export
Vulners integration fix	Deprecation-safe usage & no-crash error handling
New exploitdb_lookup module	Searches exploit titles and URLs for top CVEs
Bug bounty scan improvements	HTTPS detection and result CSV fix
AI vulnerability analysis	Structured recommendations format
Report generator	Multi-format output + safe handling
Charts	CVSS distribution ASCII graph
Telegram	File & message delivery stable
📦 Changelog
Added

exploitdb_lookup.py — ExploitDB public exploit query module

ai_risk.py — GPT-based scoring and summary

charts_ascii.py — CVSS chart rendering

Telegram document + message sending

PDF/DOCX dual output support

Updated

main.py redesigned workflow & runtime UI

bounty_scan.py signature + CSV structure

report_gen.py with combined paths + AI summary

local_scan.py simplified return model

Removed

Unused animation code

Experimental dashboard UI (moved to roadmap)

Known Issues
Issue	Status
Metasploit RPC auto-connect may fail if msfrpcd not running	Run manually on users choice
No CVE = Skips ExploitDB lookup	Working as intended
⚙ Requirements
Python 3.10+
Kali Linux / Ubuntu recommended
Nmap, Subfinder installed

🧠 API Keys Required

Located in config.json

openai.api_key
shodan.api_key
vulners.api_key
telegram.bot_token
telegram.chat_id

💀 Author & Credits

Hemanth Karal Varmaa (0xDEADVrm)
Cybersecurity Researcher | Bug Bounty Hunter | Red Team

Follow: linkedin.com/in/varmaa07

⭐ Support the Project

If you want more upgrades like:

Payload automation

Auto exploit execution

Red team C2 extension

👉 Star the repository
👉 Share in cybersecurity communities

🔥 Roadmap — v2.0 Upcoming
Feature	Status
AI Exploit recommendation engine	⏳ In progress
Web dashboard realtime	🧪 Testing
Exploit auto-exec with Metasploit	Planned
Mobile client for Telegram bot	Planning
🧨 Final Message

"The future belongs to those who automate offense."
Enjoy the hunt, 0xDEADVrm 😈🔥
