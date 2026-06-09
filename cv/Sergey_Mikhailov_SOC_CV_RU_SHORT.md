# Сергей Михайлов

## SOC Analyst / SecOps Engineer

**GitHub:** https://github.com/prodlovely88-ux 
**SOC Portfolio:** https://github.com/prodlovely88-ux/soc-portfolio 
**Windows Security Log Triage:** https://github.com/prodlovely88-ux/windows-security-log-triage 
**IOC Log Enricher:** https://github.com/prodlovely88-ux/ioc-log-enricher 
**Email:** mihajlov.sergei20017@gmail.com
**Telegram:** @L0WBORN
**Локация:** Мариуполь / готов к удалённой работе

---

## Профиль

Инженер по информационной безопасности / Аналитик SOC с 2-летним практическим опытом (проектная работа / аутсорс). Специализируюсь на анализе логов (Windows Security Logs, Sysmon, Linux), триаже инцидентов и автоматизации процессов мониторинга безопасности. Не просто смотрю в SIEM, а пишу рабочие инструменты на Python и PowerShell для выявления подозрительной активности и маппинга по матрице MITRE ATT&CK.

---

## Опыт работы

**SOC Analyst / SecOps Engineer (Проектная работа / NDA)**
*Июнь 2024 — Настоящее время (2 года)*

- Мониторинг и анализ событий безопасности (Windows Event Logs, Sysmon, Linux journalctl/auditd) на инфраструктуре заказчиков.
- Первичное расследование инцидентов (Triage), классификация алертов, отсеивание ложных срабатываний (False Positives).
- Выявление аномалий: RDP-брутфорс, скрытые вызовы PowerShell, подозрительные цепочки Parent-Child процессов, Discovery-активность.
- Разработка скриптов (Python, PowerShell) для автоматизации разбора логов.
- Интеграция с Threat Intelligence платформами (AbuseIPDB API) для автоматического обогащения индикаторов компрометации (IoC).
- Написание структурированных отчетов по инцидентам (Analyst Reports), выдача рекомендаций по локализации угроз.
- *Примечание: в связи с NDA боевые логи не разглашаются. Обезличенные версии разработанных инструментов выложены в GitHub.*

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

В портфолио оформлены SOC-кейсы:

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

Текущий этап:

- Threat Hunting, автоматизация процессов SOC и Advanced Incident Response.

---

## Английский

English: Intermediate / B1-B2.

Практикую написание SOC case reports на английском: severity, verdict, evidence, analysis, MITRE mapping, next checks, recommended actions.

---

## Цель

Найти сильную команду на позицию SOC Analyst / SecOps Engineer и развиваться в направлении Blue Team, threat detection, incident triage и security operations.
