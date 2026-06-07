# Сергей Михайлов

## Junior SOC Analyst / SOC L1 / Security Monitoring Analyst

**GitHub:** https://github.com/prodlovely88-ux 
**SOC Portfolio:** https://github.com/prodlovely88-ux/soc-portfolio 
**Windows Security Log Triage:** https://github.com/prodlovely88-ux/windows-security-log-triage 
**IOC Log Enricher:** https://github.com/prodlovely88-ux/ioc-log-enricher 
Email: mihajlov.sergei20017@gmail.com
Telegram: @L0WBORN
Локация: Мариуполь / готов к удалённой работе

---

## Профиль

Начинающий SOC-аналитик с практическим фокусом на Windows Security Logs, Sysmon, incident triage, suspicious PowerShell activity, RDP investigations, IOC analysis и автоматизацию задач мониторинга.

Работаю с практическими SOC-сценариями: анализ входов, цепочек процессов, сетевых подключений, подозрительных команд, MITRE ATT&CK mapping и оформление analyst reports.

Дополнительно развиваю технические проекты на Python и Linux, включая AI-ассистента JARVIS и коммерческий Telegram-бот, что даёт практический опыт в автоматизации, API, backend-логике, debugging и серверном развёртывании.

---

## Ключевые навыки

- Windows Security Logs: 4624, 4625, 4634, 4688
- Sysmon: Event ID 1, 3, 11
- Incident triage: noise / suspicious / incident
- Suspicious PowerShell detection
- RDP Logon Type 10 analysis
- MITRE ATT&CK basic mapping
- IOC extraction and enrichment
- Python, PowerShell, Bash
- Linux, Git, GitHub
- TCP/IP, DNS, HTTP/HTTPS
- CSV reporting, log parsing, API integration

---

## SOC-проекты

### Windows Security Log Triage

PowerShell-инструмент для анализа Windows Security Event ID 4688 и первичного triage подозрительных процессов.

Реализовано:

- анализ Parent Process → Child Process;
- detection suspicious PowerShell flags;
- поиск Discovery-команд;
- suspicious-only фильтрация;
- CSV export;
- verdict, severity, reason, triage note.

**Репозиторий:**  
https://github.com/prodlovely88-ux/windows-security-log-triage

---

### IOC Log Enricher

Python-инструмент для извлечения публичных IP-адресов из логов, контекстного triage и AbuseIPDB enrichment.

Реализовано:

- IPv4 extraction;
- фильтрация private/local/reserved IP;
- подсчёт повторений;
- context-aware verdict;
- AbuseIPDB API integration;
- human-readable console report;
- CSV export.

**Репозиторий:**  
https://github.com/prodlovely88-ux/ioc-log-enricher

---

## Case Studies

В портфолио оформлены практические SOC-кейсы:

- **Benign Printer Activity** - корректное закрытие benign alert без лишней эскалации.
- **RDP and PowerShell Investigation** - failed logins → successful RDP login → PowerShell activity, verdict: suspicious, context required.
- **Office Malware Incident** - Microsoft Office → PowerShell → Temp script → external connection → persistence, verdict: CRITICAL / confirmed incident.

**Портфолио:**  
https://github.com/prodlovely88-ux/soc-portfolio

---

## Дополнительные проекты

### JARVIS AI Assistant

Персональный AI-ассистент для Arch Linux / Wayland на Python.

Ключевые элементы:

- voice input / wake-word workflow;
- ASR / TTS integration;
- LLM API integration;
- screenshot / vision pipeline;
- controlled command execution;
- подтверждение рискованных действий;
- Linux desktop automation;
- debugging latency, audio streams, API requests и локальных сервисов.

Релевантность: Python engineering, Linux automation, API integration, command execution safety, debugging complex multi-file systems.

### Commercial Telegram Ordering Bot

Коммерческий Telegram-бот для кофейни с заказами, оплатой и серверным развёртыванием.

Реализовано:

- Telegram bot workflow;
- меню, корзина, checkout;
- payment integration;
- webhook processing;
- VPS deployment;
- nginx / systemd / domain setup;
- debugging production-сценариев.

---

## Практическое обучение

Фокус:

- Network Fundamentals
- Linux for Security
- Windows Security Logs
- Sysmon
- MITRE ATT&CK
- SOC triage methodology
- Incident reporting
- SIEM fundamentals
- Detection rules and use cases

Текущий этап: SIEM basics, alert triage, detection logic, practical SOC investigations.

---

## Английский

English: Intermediate / B1-B2.

Практикую написание SOC case reports на английском: severity, verdict, evidence, analysis, MITRE mapping, next checks, recommended actions.

---

## Цель

Junior SOC Analyst / SOC L1 / Security Monitoring Analyst. Развитие в Blue Team, threat detection, incident triage и security operations.
