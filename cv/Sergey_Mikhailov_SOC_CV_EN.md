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
Current focus:

Continuous skill enhancement in Threat Hunting, Advanced Incident Response, and automation.

---

## English

English: Intermediate / B1-B2

I practice writing SOC case reports in English, including severity, verdict, evidence, analysis, MITRE mapping, next checks, and recommended actions.

---

## Career Objective

Seeking a SOC Analyst / SecOps Engineer / Security Monitoring Analyst position with further development in Blue Team operations
