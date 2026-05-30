# Sergey Mikhailov

## Junior SOC Analyst / SOC L1 / Security Monitoring Analyst

**GitHub:** https://github.com/prodlovely88-ux 
**SOC Portfolio:** https://github.com/prodlovely88-ux/soc-portfolio 
**Windows Security Log Triage:** https://github.com/prodlovely88-ux/windows-security-log-triage 
**IOC Log Enricher:** https://github.com/prodlovely88-ux/ioc-log-enricher 
**Email:** mihajlov.sergei20017@gmail.com 
**Telegram:** @L0WBORN
**Location:** Mariupol / open to remote work

---

## Profile

Entry-level SOC analyst focused on security event analysis, Windows Security Logs, Sysmon, suspicious activity triage, and security monitoring automation.

I practice Windows event investigation, process chain analysis, suspicious PowerShell review, RDP activity analysis, IOC extraction/enrichment, and MITRE ATT&CK mapping.

I also build practical technical projects with Python and Linux, including the JARVIS AI assistant and a commercial Telegram ordering bot. These projects provide hands-on experience with automation, API integration, backend logic, server deployment, debugging, and controlled command execution.

Main areas of interest: Blue Team operations, Security Monitoring, Threat Detection, Incident Triage, and SOC Analyst / Detection Engineering development.

---

## Core Skills

### SOC / Security Monitoring

- Initial security event triage
- Noise / suspicious / incident classification
- Evidence-based log analysis
- Analyst verdict writing
- Next checks and recommended actions
- Investigation reports and case studies
- Confirmed incident vs suspicious activity separation

### Windows Security Logs

- Event ID 4624 - Successful Logon
- Event ID 4625 - Failed Logon
- Event ID 4634 - Logoff
- Event ID 4688 - Process Creation
- Logon Type analysis
- RDP Logon Type 10 review
- Correlation by time and Logon ID
- Process creation and command-line analysis

### Sysmon

- Sysmon Event ID 1 - Process Create
- Sysmon Event ID 3 - Network Connection
- Sysmon Event ID 11 - File Create
- ProcessGuid correlation
- Process Create → Network Connection → File Create analysis
- Suspicious path analysis: Temp, AppData, Downloads, Public
- Office → PowerShell investigation scenarios

### Threat Detection / MITRE ATT&CK

- Suspicious PowerShell detection
- Discovery activity detection
- Persistence indicators
- Possible lateral movement indicators
- Basic MITRE ATT&CK mapping
- Confirmed vs possible mapping separation

### Automation / Scripting

- Python
- PowerShell
- Bash
- CSV reporting
- Log parsing
- API integration
- Git / GitHub
- `.env` and API key handling
- CLI tool and service debugging

### Systems and Networking

- Windows
- Linux
- TCP/IP
- DNS
- HTTP/HTTPS
- Basic network activity analysis
- VPS / nginx / systemd basics

---

## Practical SOC Projects

### Windows Security Log Triage

**Repository:** https://github.com/prodlovely88-ux/windows-security-log-triage

PowerShell-based tool for analyzing Windows Security Event ID 4688 and performing initial triage of suspicious process activity.

Implemented features:

- Process Creation event parsing;
- Parent Process → Child Process analysis;
- detection of suspicious PowerShell parameters:
  - `-NoProfile`
  - `-ExecutionPolicy Bypass`
  - `-EncodedCommand`
  - `-WindowStyle Hidden`
- Discovery command detection;
- suspicious-only filtering;
- CSV export;
- verdict, severity, reason, and triage note fields.

This project demonstrates:

- Windows Security Logs understanding;
- practical process triage;
- ability to automate repetitive SOC tasks;
- structured analysis reporting.

---

### IOC Log Enricher

**Repository:** https://github.com/prodlovely88-ux/ioc-log-enricher

Python-based tool for extracting public IP addresses from logs, performing context-aware IOC triage, and enriching indicators with AbuseIPDB reputation data.

Implemented features:

- IPv4 extraction from logs;
- filtering private, local, and reserved IP addresses using `ipaddress`;
- indicator frequency counting;
- log line context analysis;
- verdict logic: HIGH / SUSPICIOUS / CHECK / INFO;
- AbuseIPDB API enrichment;
- secure API key handling through `.env`;
- human-readable console report;
- CSV export.

This project demonstrates:

- Python automation;
- log analysis;
- IOC triage;
- threat intelligence enrichment;
- practical indicator analysis workflow.

---

## Investigation Case Studies

**Portfolio:** https://github.com/prodlovely88-ux/soc-portfolio

Practical case studies written in SOC triage / analyst report format.

### Benign Printer Activity

- Classification of legitimate network activity
- Separation of benign activity from suspicious activity
- Alert closure without unnecessary escalation after context validation

### RDP and PowerShell Investigation

- Analysis of 12 failed logins followed by successful RDP login
- Event ID 4625 / 4624
- Logon Type 10
- Source IP validation
- PowerShell activity with risky flags
- Verdict: suspicious, context required

### Office Malware Incident

- Microsoft Office → PowerShell → Temp script → external connection → persistence chain
- Suspicious PowerShell flags
- External IP connection
- Persistence indicators
- Verdict: CRITICAL / confirmed incident
- Recommendations for isolation, evidence preservation, and escalation

---

## Additional Technical Projects

### JARVIS AI Assistant

Personal AI assistant for Arch Linux / Wayland, developed in Python as a modular desktop automation system.

Key project components:

- voice input and wake-word workflow;
- ASR / TTS integration;
- LLM API integration;
- screen context handling through screenshot / vision pipeline;
- system command execution through a controlled command execution flow;
- confirmation logic before potentially risky actions;
- modular tool architecture;
- Linux desktop automation;
- Git-based development workflow;
- debugging of latency, audio streams, API requests, and local services.

Relevance to SOC / IT:

- Python engineering;
- Linux automation;
- API integration;
- safe command execution logic;
- system context handling;
- debugging of a complex multi-file system;
- understanding risks around automation and command execution.

---

### Commercial Telegram Ordering Bot

Commercial Telegram ordering bot for a coffee shop with order workflow, payment integration, and server deployment.

Implemented areas:

- Telegram bot workflow;
- menu, cart, and checkout logic;
- payment integration;
- webhook processing;
- VPS deployment;
- domain, nginx, and systemd configuration;
- debugging and production scenario testing.

Relevance to SOC / IT:

- backend logic experience;
- API integration;
- Linux server workflow;
- deployment and debugging;
- practical understanding of service operations.

---

## Practical Training

Training focus areas:

- Network Fundamentals
- Linux for Security
- Windows Security Logs
- Sysmon
- MITRE ATT&CK
- SOC triage methodology
- Incident reporting
- SIEM fundamentals
- Detection rules and use cases

Current focus:

- SIEM basics
- Alert triage
- Detection logic
- Practical SOC investigations
- Preparation for Junior SOC / SOC L1 roles

---

## English

English: Intermediate / B1-B2

I practice writing SOC case reports in English, including severity, verdict, evidence, analysis, MITRE mapping, next checks, and recommended actions.

---

## Career Objective

Seeking a Junior SOC Analyst / SOC L1 / Security Monitoring Analyst position with further development in Blue Team operations, threat detection, incident triage, and security operations.
