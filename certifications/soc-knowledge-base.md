# SOC Knowledge Base & Playbooks

## Русская версия

## SOC / Blue Team Core Competencies

Этот репозиторий — моя личная база знаний (Knowledge Base) и структура компетенций по направлениям SOC, Blue Team, анализа логов и Threat Hunting.

Здесь я систематизирую рабочий опыт, разбираю сложные вектора атак, документирую плейбуки (Playbooks) для триажа и храню логику написания кастомных скриптов автоматизации.

---

## Core Operations & Tech Stack

### Network Traffic Analysis & Investigations
Сетевая криминалистика и анализ аномалий:
- Глубокое понимание OSI / TCP-IP, TCP/UDP.
- Разбор протоколов прикладного уровня: DNS (туннелирование, аномальные запросы), DHCP, HTTP / HTTPS.
- Идентификация Beaconing-активности и C2-трафика.
- Инструментарий: tcpdump, Wireshark, tshark, nmap, curl, встроенные утилиты ОС (netstat, ss).

### Linux Security & SecOps
Харденинг, мониторинг и хантинг в *nix-средах:
- Мониторинг системных логов: auditd, journalctl, auth.log, syslog.
- Расследование инцидентов: анализ bash_history, поиск скрытых файлов, проверка cron-задач и подозрительных systemd-сервисов.
- Управление правами доступа (SUID/SGID биты, chown/chmod) и поиск misconfigurations.
- Разработка Bash-скриптов для автоматизации сбора артефактов при инцидентах.

### Windows Security & Sysmon
Анализ поведения в Windows-инфраструктуре:
- Triage базовых событий Windows Security Event Logs (4624, 4625, 4688, 4698, 4720 и др.).
- Глубокий анализ телеметрии Sysmon (Event ID 1, 3, 7, 8, 11, 22).
- Выявление аномалий PowerShell (ExecutionPolicy Bypass, EncodedCommand, скрытые окна).
- Охота за закреплением (Persistence): реестр, планировщик задач, службы, папки автозагрузки.

### SIEM Operations & Alert Triage
Практическая работа с инцидентами:
- Жизненный цикл инцидента: Event → Alert → Triage → Incident Response.
- Отсеивание False Positives и контекстный анализ сработок.
- Маппинг выявленных техник на матрицу MITRE ATT&CK.
- Разработка Detection Rules и Use Cases под новые угрозы.
- Написание структурированных Analyst Reports на английском языке.

---

## Типовые Плейбуки (Playbooks)

В рамках операционной работы я формализую подходы к расследованию следующих сценариев:
- RDP-брутфорс с последующим закреплением и Discovery-командами.
- Вредоносная активность через офисные макросы (Office → PowerShell → Temp script → C2).
- Выявление аномальных сетевых соединений (отсев легитимного трафика от потенциального ботнета/C2).
- Анализ цепочек процессов (Parent-Child Process Injection).

---

## Инструментарий и Автоматизация (Projects)

Собственные разработки для снижения рутины в SOC:
- **Windows Security Log Triage:** Утилита на PowerShell для парсинга Event ID 4688 и выявления аномальных цепочек процессов.
- **IOC Log Enricher:** Python-скрипт для автоматического извлечения IP-адресов из сырых логов и их контекстного обогащения через AbuseIPDB API.

---

## Current Focus
Continuous professional development: Threat Hunting, Advanced Incident Response, SOC automation and Malware Analysis.
