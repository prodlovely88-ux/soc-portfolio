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

### SOC / Security Monitoring

- Первичный triage событий безопасности
- Классификация событий: noise / suspicious / incident
- Анализ evidence из логов
- Формирование analyst verdict
- Описание next checks и recommended actions
- Подготовка investigation reports / case studies
- Разделение confirmed incident и suspicious activity

### Windows Security Logs

- Event ID 4624 - Successful Logon
- Event ID 4625 - Failed Logon
- Event ID 4634 - Logoff
- Event ID 4688 - Process Creation
- Анализ Logon Type
- Анализ RDP Logon Type 10
- Корреляция событий по времени и Logon ID
- Анализ process creation и command line

### Sysmon

- Sysmon Event ID 1 - Process Create
- Sysmon Event ID 3 - Network Connection
- Sysmon Event ID 11 - File Create
- ProcessGuid correlation
- Анализ цепочек Process Create → Network Connection → File Create
- Анализ подозрительных путей: Temp, AppData, Downloads, Public
- Office → PowerShell investigation scenarios

### Threat Detection / MITRE ATT&CK

- Suspicious PowerShell detection
- Discovery activity detection
- Persistence indicators
- Possible lateral movement indicators
- Basic MITRE ATT&CK mapping
- Разделение confirmed и possible mapping

### Automation / Scripting

- Python
- PowerShell
- Bash
- CSV reporting
- Log parsing
- API integration
- Git / GitHub
- Работа с `.env` и API-ключами
- Отладка CLI-инструментов и сервисов

### Системы и сети

- Windows
- Linux
- TCP/IP
- DNS
- HTTP/HTTPS
- Базовый анализ сетевой активности
- VPS / nginx / systemd basics

---

## Практические SOC-проекты

### Windows Security Log Triage

**Репозиторий:** https://github.com/prodlovely88-ux/windows-security-log-triage

PowerShell-инструмент для анализа Windows Security Event ID 4688 и первичного triage подозрительных процессов.

Реализовано:

- парсинг событий Process Creation;
- анализ Parent Process → Child Process;
- выявление подозрительных параметров PowerShell:
  - `-NoProfile`
  - `-ExecutionPolicy Bypass`
  - `-EncodedCommand`
  - `-WindowStyle Hidden`
- обнаружение Discovery-команд;
- suspicious-only фильтрация;
- CSV export;
- verdict, severity, reason и triage note.

Что показывает проект:

- понимание Windows Security Logs;
- практический process triage;
- умение автоматизировать повторяющиеся SOC-задачи;
- способность оформлять результаты анализа.

---

### IOC Log Enricher

**Репозиторий:** https://github.com/prodlovely88-ux/ioc-log-enricher

Python-инструмент для извлечения публичных IP-адресов из логов, контекстного анализа IOC и enrichment через AbuseIPDB.

Реализовано:

- извлечение IPv4 из логов;
- фильтрация private/local/reserved IP через `ipaddress`;
- подсчёт повторений индикаторов;
- анализ контекста строк логов;
- verdict logic: HIGH / SUSPICIOUS / CHECK / INFO;
- AbuseIPDB API enrichment;
- безопасная работа с API-ключом через `.env`;
- человекочитаемый console report;
- CSV export.

Что показывает проект:

- Python automation;
- log analysis;
- IOC triage;
- threat intelligence enrichment;
- практический подход к анализу индикаторов.

---

## Investigation Case Studies

**Портфолио:** https://github.com/prodlovely88-ux/soc-portfolio

Оформлены практические case studies в формате SOC triage / analyst report.

### Benign Printer Activity

- Классификация легитимной сетевой активности
- Разделение benign activity и suspicious activity
- Закрытие alert без лишней эскалации после проверки контекста

### RDP and PowerShell Investigation

- Анализ 12 failed logins и последующего successful RDP login
- Event ID 4625 / 4624
- Logon Type 10
- Проверка Source IP
- PowerShell activity с risky flags
- Verdict: suspicious, context required

### Office Malware Incident

- Цепочка Microsoft Office → PowerShell → Temp script → external connection → persistence
- Suspicious PowerShell flags
- External IP connection
- Persistence indicators
- Verdict: CRITICAL / confirmed incident
- Рекомендации по изоляции, сбору артефактов и эскалации

---

## Дополнительные технические проекты

### JARVIS AI Assistant

Персональный AI-ассистент для Arch Linux / Wayland, разрабатываемый на Python как модульная система автоматизации рабочего окружения.

Ключевые элементы проекта:

- голосовой ввод и wake-word workflow;
- интеграция ASR / TTS;
- взаимодействие с LLM через API;
- обработка контекста экрана через screenshot / vision pipeline;
- выполнение системных команд через контролируемый command execution flow;
- подтверждение потенциально рискованных действий перед запуском;
- модульная архитектура инструментов;
- работа с Linux desktop automation;
- Git-based workflow и поэтапная разработка функций;
- отладка latency, аудио-потоков, API-запросов и локальных сервисов.

Релевантность для SOC / IT:

- Python engineering;
- Linux automation;
- API integration;
- безопасная логика выполнения команд;
- работа с системным контекстом;
- debugging сложной многофайловой системы;
- понимание risks around automation and command execution.

---

### Commercial Telegram Ordering Bot

Коммерческий Telegram-бот для кофейни с интеграцией заказов, оплатой и серверным развёртыванием.

Что было реализовано:

- Telegram bot workflow;
- меню, корзина и оформление заказа;
- интеграция с оплатой;
- webhook processing;
- серверное развёртывание на VPS;
- работа с доменом, nginx и systemd;
- обработка ошибок и тестирование production-сценариев.

Релевантность для SOC / IT:

- опыт работы с backend-логикой;
- API integration;
- Linux server workflow;
- deployment/debugging;
- понимание практической эксплуатации сервиса.

---

## Практическое обучение

Текущий этап:

- Фокус развития: Threat Hunting, автоматизация процессов SOC и Advanced Incident Response.

---

## Английский язык

English: Intermediate / B1-B2

Практикую написание SOC case reports на английском языке: severity, verdict, evidence, analysis, MITRE mapping, next checks и recommended actions.

---

## Цель
Найти сильную команду на позицию SOC Analyst / SecOps Engineer и развиваться в направлении Blue Team, threat detection, incident triage и security operations.
