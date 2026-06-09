# Сергей Михайлов

## SOC Analyst / SecOps Engineer

Портфолио по информационной безопасности с фокусом на SecOps, анализ событий безопасности, расследование инцидентов и автоматизацию процессов мониторинга. 

2 года практического опыта работы в рамках коммерческого аутсорса (под NDA). Основная специализация: триаж и глубокий анализ алертов, выявление комплексных векторов атак (от Initial Access до Persistence), написание кастомной логики детектирования и автоматизация SOC-рутины на Python/PowerShell.

---

## CV / Резюме

- [Короткое резюме RU, PDF](cv/export/Sergey_Mikhailov_SOC_CV_RU_SHORT.pdf)
- [Short CV EN, PDF](cv/export/Sergey_Mikhailov_SOC_CV_EN_SHORT.pdf)

- [Полное резюме на русском](cv/Sergey_Mikhailov_SOC_CV_RU.md)
- [Full CV in English](cv/Sergey_Mikhailov_SOC_CV_EN.md)

---

## Ключевой технический стек (Core Skills)

- SIEM & EDR Operations: Работа со связкой Wazuh + ELK Stack (Elasticsearch, Logstash, Kibana), написание KQL-запросов, кастомные дашборды. -> [Детальнее](skills/siem-elk-wazuh.md)
- Windows Security Logs: Глубокий анализ Event ID 4624, 4625, 4688, 4698, корреляция событий по Logon ID. -> [Детальнее](skills/windows-security-logs.md)
- Sysmon Telemetry: Анализ поведения процессов (Event ID 1, 3, 11), выявление аномальных цепочек Parent-Child. -> [Детальнее](skills/sysmon.md)
- Network Traffic Analysis: Разбор PCAP-дампов (Wireshark/tshark), выявление C2-трафика и beaconing-активности. -> [Детальнее](skills/network-analysis.md)
- Threat Intelligence & OSINT: Автоматизация обогащения IoC (API AbuseIPDB, VirusTotal), работа с песочницами (ANY.RUN). -> [Детальнее](skills/threat-intel.md)
- MITRE ATT&CK Mapping: Привязка активности атакующих к тактикам и техникам в рамках Analyst Reports. -> [Детальнее](skills/mitre-attck.md)
- Linux SecOps: Работа в консоли Arch Linux, аудит логов (auditd, journalctl), автоматизация на Bash/Python. -> [Детальнее](skills/linux.md)

---

## Проекты и Инженерная практика (Projects)

Реальные инструменты и коммерческие сервисы, разработанные для оптимизации инфраструктуры и автоматизации SecOps/IT процессов (инструменты безопасности полностью обезличены и вынесены из-под NDA в open-source):

### Инструменты ИБ / Мониторинга (SecOps Tools)
1. **[Windows Security Log Triage](projects/windows-security-log-triage.md)** — PowerShell-утилита для парсинга Event ID 4688, выявления аномальных флагов PowerShell (`-EncodedCommand`, `-Bypass`) и корреляции цепочек процессов.
2. **[IOC Log Enricher](projects/ioc-log-enricher.md)** — Python-скрипт для автоматического извлечения публичных IPv4-адресов из логов и их контекстного обогащения через AbuseIPDB API с генерацией финального вердикта.

### Разработка и Системная автоматизация (Engineering & Automation)
3. **JARVIS (Personal AI Assistant)** — Персональный ИИ-ассистент, глубоко интегрированный в рабочее окружение Arch Linux / Wayland. Написан на Python. Отрабатывает задачи автоматизации рабочего стола, управления системным контекстом и безопасного выполнения команд с логикой подтверждения перед рискованными действиями. 
   - *Релевантность для SOC:* Опыт построения сложных многофайловых систем, обработка API-запросов, парсинг логов latency, написание безопасных системных скриптов управления окружением.
4. **Commercial Telegram Ordering Bot** — Коммерческий бэкенд-сервис для автоматизации заказов кофейни с полноценным workflow, интеграцией платежного шлюза и развертыванием на боевом сервере.
   - *Релевантность для SOC:* Практический опыт настройки Linux-серверов (VPS), развертывание и конфигурация веб-серверов (Nginx, reverse proxy), управление системными демонами (Systemd), логирование и обработка вебхуков. Понимание логики работы веб-приложений изнутри помогает эффективнее выявлять атаки на веб-инфру.

---

## Разбор инцидентов (Case Studies)

Примеры структурированных тикетов (Analyst Reports) по результатам расследования реальных кейсов:
- **[Case 01: Benign Printer Activity](case-studies/case-01-benign-printer-activity.md)** — Анализ ложноположительного срабатывания (False Positive) при сетевой активности принтера.
- **[Case 02: RDP and PowerShell Investigation](case-studies/case-02-rdp-powershell-investigation.md)** — Расследование подозрительного ночного RDP-входа с последующей Discovery-активностью через PowerShell.
- **[Case 03: Office Malware Incident](case-studies/case-03-office-malware-incident.md)** — Настоящий инцидент: макрос Word -> скрытый запуск PowerShell -> Temp script -> C2 соединение -> попытка закрепления.

---

## База знаний и регламенты (Knowledge Base)

Личная системная база знаний и плейбуки (Playbooks), используемые для оперативной работы на смене:
- **[SOC Knowledge Base & Playbooks](skills/soc-knowledge-base.md)**

---

## Контакты

- Email: mihajlov.sergei20017@gmail.com
- Telegram: @L0WBORN
