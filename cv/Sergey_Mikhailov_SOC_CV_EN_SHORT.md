# Sergey Mikhailov

## SOC Analyst / SecOps Engineer

GitHub: https://github.com/prodlovely88-ux 
SOC Portfolio: https://github.com/prodlovely88-ux/soc-portfolio 
Windows Security Log Triage: https://github.com/prodlovely88-ux/windows-security-log-triage 
IOC Log Enricher: https://github.com/prodlovely88-ux/ioc-log-enricher 
Email: mihajlov.sergei20017@gmail.com
Telegram: @L0WBORN
Location: Mariupol / open to remote work

---

## Profile

SOC Analyst / SecOps Engineer with 2 years of practical experience (contract/outsource). Focused on log analysis (Windows Security Logs, Sysmon, Linux), incident triage, and security monitoring automation. I don't just monitor SIEM alerts; I develop functional tools in Python and PowerShell to detect suspicious activity, automate routine tasks, and map threats to the MITRE ATT&CK framework.

---

## Experience

SOC Analyst / SecOps Engineer (Contract / NDA)
June 2024 — Present (2 years)

- Monitored and analyzed security events across client infrastructure using Windows Event Logs, Sysmon, and Linux logs.
- Performed initial incident triage, classified alerts, and filtered false positives.
- Detected anomalies including RDP brute-force attempts, hidden PowerShell executions, suspicious Parent-Child process chains, and Discovery activities.
- Developed Python and PowerShell scripts to automate log parsing and routine checks.
- Integrated Threat Intelligence platforms (AbuseIPDB API) for automated IOC enrichment.
- Authored structured Analyst Reports and provided recommendations for threat containment.
- Note: Due to NDA restrictions, production logs and client details cannot be disclosed. Sanitized versions of the automation tools I developed are available on my GitHub.

---
## Core Skills

- Windows Security Logs: 4624, 4625, 4634, 4688
- Sysmon: Event ID 1, 3, 11
- Incident triage: noise / suspicious / incident
- Suspicious PowerShell detection
- RDP Logon Type 10 analysis
- Basic MITRE ATT&CK mapping
- IOC extraction and enrichment
- Python, PowerShell, Bash
- Linux, Git, GitHub
- TCP/IP, DNS, HTTP/HTTPS
- CSV reporting, log parsing, API integration

---

## SOC Projects

### Windows Security Log Triage

PowerShell-based tool for analyzing Windows Security Event ID 4688 and performing initial triage of suspicious process activity.

Implemented:

- Parent Process → Child Process analysis;
- suspicious PowerShell flag detection;
- Discovery command identification;
- suspicious-only filtering;
- CSV export;
- verdict, severity, reason, and triage note fields.

**Repository:**  
https://github.com/prodlovely88-ux/windows-security-log-triage

---

### IOC Log Enricher

Python-based tool for extracting public IP addresses from logs, performing context-aware triage, and enriching indicators with AbuseIPDB reputation data.

Implemented:

- IPv4 extraction;
- filtering private, local, and reserved IP addresses;
- indicator frequency counting;
- context-aware verdict logic;
- AbuseIPDB API integration;
- human-readable console report;
- CSV export.

**Repository:**  
https://github.com/prodlovely88-ux/ioc-log-enricher

---

## Case Studies

The portfolio includes practical SOC investigation write-ups:

- **Benign Printer Activity** - correct benign alert closure without unnecessary escalation.
- **RDP and PowerShell Investigation** - failed logins → successful RDP login → PowerShell activity, verdict: suspicious, context required.
- **Office Malware Incident** - Microsoft Office → PowerShell → Temp script → external connection → persistence, verdict: CRITICAL / confirmed incident.

**Portfolio:**  
https://github.com/prodlovely88-ux/soc-portfolio

---

## Additional Projects

### JARVIS AI Assistant

Personal AI assistant for Arch Linux / Wayland developed in Python.

Key components:

- voice input / wake-word workflow;
- ASR / TTS integration;
- LLM API integration;
- screenshot / vision pipeline;
- controlled command execution;
- confirmation logic before risky actions;
- Linux desktop automation;
- debugging latency, audio streams, API requests, and local services.

Relevance: Python engineering, Linux automation, API integration, command execution safety, debugging complex multi-file systems.

### Commercial Telegram Ordering Bot

Commercial Telegram ordering bot for a coffee shop with ordering workflow, payment integration, and server deployment.

Implemented:

- Telegram bot workflow;
- menu, cart, checkout;
- payment integration;
- webhook processing;
- VPS deployment;
- nginx / systemd / domain setup;
- production scenario debugging.

---

## Practical Training

Current focus: 
Continuous skill enhancement in Threat Hunting, Advanced Incident Response, and automation.

---

## English

English: Intermediate / B1-B2.

I practice writing SOC case reports in English: severity, verdict, evidence, analysis, MITRE mapping, next checks, and recommended actions.

---

## Career Objective

Seeking a SOC Analyst / SecOps Engineer / Security Monitoring Analyst position with further development in Blue Team operations
