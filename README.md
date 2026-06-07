# Сергей Михайлов

## Junior SOC Analyst / Security Monitoring

Портфолио по информационной безопасности с фокусом на SOC, анализ событий безопасности, расследование подозрительной активности и автоматизацию задач мониторинга.

Я развиваюсь в направлении Blue Team и практикую подход, близкий к реальной работе SOC-аналитика: анализ логов, triage событий, построение цепочек активности, проверка гипотез, MITRE ATT&CK mapping и оформление выводов в формате analyst report.

---

## CV / Резюме

- [Короткое резюме RU, PDF](cv/export/Sergey_Mikhailov_Junior_SOC_CV_RU_SHORT.pdf)
- [Короткое резюме RU, DOCX](cv/export/Sergey_Mikhailov_Junior_SOC_CV_RU_SHORT.docx)
- [Short CV EN, PDF](cv/export/Sergey_Mikhailov_Junior_SOC_CV_EN_SHORT.pdf)
- [Short CV EN, DOCX](cv/export/Sergey_Mikhailov_Junior_SOC_CV_EN_SHORT.docx)

- [Полное резюме на русском](cv/Sergey_Mikhailov_Junior_SOC_CV_RU.md)
- [Full CV in English](cv/Sergey_Mikhailov_Junior_SOC_CV_EN.md)

---

## Ключевой фокус

- Windows Security Logs analysis
- Sysmon investigation
- Incident triage
- Suspicious PowerShell detection
- RDP activity analysis
- IOC extraction and enrichment
- MITRE ATT&CK mapping
- Python / PowerShell automation
- Linux-based workflow
- Security monitoring fundamentals
- SIEM alert triage
- Detection logic and SOC use cases
- Analyst ticket writing
- Severity assessment and escalation logic

---

## Проекты

### [Windows Security Log Triage](projects/windows-security-log-triage.md)

PowerShell-инструмент для анализа Windows Security Event ID 4688 и первичного triage подозрительных процессов.

**Что реализовано:**

- анализ событий Process Creation;
- разбор цепочек Parent Process → Child Process;
- выявление подозрительных параметров PowerShell;
- поиск Discovery-команд;
- suspicious-only фильтрация;
- CSV-отчёт для дальнейшего анализа.

**Навыки:** Windows Security Logs, Event ID 4688, PowerShell, process analysis, SOC triage.

**Репозиторий:**  
https://github.com/prodlovely88-ux/windows-security-log-triage

---

### [IOC Log Enricher](projects/ioc-log-enricher.md)

Python-инструмент для извлечения публичных IP-адресов из логов, контекстного анализа IOC и обогащения данных через AbuseIPDB.

**Что реализовано:**

- извлечение IPv4 из логов;
- фильтрация private/local/reserved адресов;
- подсчёт повторений индикаторов;
- контекстный анализ строк логов;
- AbuseIPDB enrichment;
- человекочитаемый console report;
- экспорт результата в CSV.

**Навыки:** Python, log analysis, IOC triage, threat intelligence, AbuseIPDB API, CSV reporting.

**Репозиторий:**  
https://github.com/prodlovely88-ux/ioc-log-enricher

---

## Кейсы расследований

Практические case studies оформлены в формате SOC triage / analyst report: severity, verdict, evidence, analysis, MITRE ATT&CK, next checks и recommended actions.

### [Case 01: Benign Printer Activity](case-studies/case-01-benign-printer-activity.md)

Разбор легитимной сетевой активности, связанной с обращением пользователя к принтеру.

**Что показывает кейс:**

- умение отличать benign activity от подозрительной активности;
- аккуратный triage без ложной эскалации;
- понимание контекста сетевых событий.

---

### [Case 02: RDP and PowerShell Investigation](case-studies/case-02-rdp-powershell-investigation.md)

Анализ нескольких failed logins с последующим successful RDP login и запуском PowerShell.

**Что показывает кейс:**

- анализ Event ID 4624 / 4625;
- разбор Logon Type 10;
- проверка подозрительной RDP-активности;
- анализ PowerShell с risky flags;
- разделение suspicious activity и confirmed incident.

---

### [Case 03: Office Malware Incident](case-studies/case-03-office-malware-incident.md)

Расследование цепочки Microsoft Office → PowerShell → Temp script → external connection → persistence.

**Что показывает кейс:**

- анализ suspicious process chain;
- выявление PowerShell abuse patterns;
- оценка внешнего подключения;
- определение persistence indicators;
- формирование CRITICAL verdict;
- рекомендации по изоляции и эскалации.

---

## Практические навыки

### SIEM / Alert Triage

- разбор SIEM-алертов;
- понимание логики detection rules;
- оценка severity;
- разделение false positive / true positive;
- принятие решения по эскалации;
- оформление analyst ticket;
- расследование по цепочке: alert → evidence → verdict → action.


### Security Monitoring

- первичный triage alert-ов;
- разделение noise / suspicious / incident;
- анализ evidence из логов;
- построение analyst verdict;
- оформление next checks и recommended actions.

### Windows Security Logs

- Event ID 4624, 4625, 4634, 4688;
- анализ успешных и неуспешных входов;
- Logon Type analysis;
- RDP activity investigation;
- process creation analysis;
- correlation by time and Logon ID.

Подробнее: [Windows Security Logs](skills/windows-security-logs.md)

### Sysmon

- Event ID 1: Process Create;
- Event ID 3: Network Connection;
- Event ID 11: File Create;
- ProcessGuid correlation;
- Process Create → Network Connection → File Create analysis;
- Office → PowerShell investigation scenarios.

Подробнее: [Sysmon](skills/sysmon.md)

### MITRE ATT&CK

- Execution;
- Persistence;
- Discovery;
- Lateral Movement;
- Command and Control;
- Initial Access;
- confirmed vs possible mapping.

Подробнее: [MITRE ATT&CK](skills/mitre-attck.md)

### Linux / Automation

- Linux terminal workflow;
- Git;
- Bash basics;
- Python scripting;
- PowerShell scripting;
- log parsing;
- CSV reporting;
- API integration.

Подробнее: [Linux](skills/linux.md)

---

## Текущий вектор развития

Сейчас основной фокус направлен на:
- threat hunting basics;
- incident response workflow;
- практические расследования;
- подготовку к Junior SOC / SOC L1 / Security Monitoring позициям.

Подробнее: [Learning Progress](certifications/learning-progress.md)

---

## Цель

Получить позицию Junior SOC Analyst / SOC L1 / Security Monitoring Analyst и развиваться в направлении Blue Team, threat detection, incident triage и security operations.

---

# Sergey Mikhailov

## Junior SOC Analyst / Security Monitoring

Cybersecurity portfolio focused on SOC operations, security event analysis, suspicious activity investigation, and security monitoring automation.

I am building practical Blue Team skills through log analysis, event triage, investigation workflows, activity chain reconstruction, MITRE ATT&CK mapping, and structured analyst reporting.


---

## CV / Resume

- [Short CV RU, PDF](cv/export/Sergey_Mikhailov_Junior_SOC_CV_RU_SHORT.pdf)
- [Short CV RU, DOCX](cv/export/Sergey_Mikhailov_Junior_SOC_CV_RU_SHORT.docx)
- [Short CV EN, PDF](cv/export/Sergey_Mikhailov_Junior_SOC_CV_EN_SHORT.pdf)
- [Short CV EN, DOCX](cv/export/Sergey_Mikhailov_Junior_SOC_CV_EN_SHORT.docx)

- [Full CV in Russian](cv/Sergey_Mikhailov_Junior_SOC_CV_RU.md)
- [Full CV in English](cv/Sergey_Mikhailov_Junior_SOC_CV_EN.md)

---


## Core Focus

- Windows Security Logs analysis
- Sysmon investigation
- Incident triage
- Suspicious PowerShell detection
- RDP activity analysis
- IOC extraction and enrichment
- MITRE ATT&CK mapping
- Python / PowerShell automation
- Linux-based workflow
- Security monitoring fundamentals
- SIEM alert triage
- Detection logic and SOC use cases
- Analyst ticket writing
- Severity assessment and escalation logic
---

## Projects

### [Windows Security Log Triage](projects/windows-security-log-triage.md)

PowerShell-based tool for analyzing Windows Security Event ID 4688 and performing initial triage of suspicious process activity.

**Implemented features:**

- Process Creation event analysis;
- Parent Process → Child Process chain analysis;
- suspicious PowerShell flag detection;
- Discovery command identification;
- suspicious-only filtering;
- CSV report generation.

**Skills:** Windows Security Logs, Event ID 4688, PowerShell, process analysis, SOC triage.

**Repository:**  
https://github.com/prodlovely88-ux/windows-security-log-triage

---

### [IOC Log Enricher](projects/ioc-log-enricher.md)

Python-based tool for extracting public IP addresses from logs, performing context-aware IOC triage, and enriching indicators with AbuseIPDB reputation data.

**Implemented features:**

- IPv4 extraction from logs;
- filtering of private, local, and reserved addresses;
- indicator frequency counting;
- log line context analysis;
- AbuseIPDB enrichment;
- human-readable console report;
- CSV export.

**Skills:** Python, log analysis, IOC triage, threat intelligence, AbuseIPDB API, CSV reporting.

**Repository:**  
https://github.com/prodlovely88-ux/ioc-log-enricher

---

## Investigation Case Studies

Practical case studies are written in a SOC triage / analyst report format: severity, verdict, evidence, analysis, MITRE ATT&CK, next checks, and recommended actions.

### [Case 01: Benign Printer Activity](case-studies/case-01-benign-printer-activity.md)

Analysis of legitimate network activity related to user access to a printer.

**This case demonstrates:**

- ability to distinguish benign activity from suspicious activity;
- careful triage without unnecessary escalation;
- understanding of network event context.

---

### [Case 02: RDP and PowerShell Investigation](case-studies/case-02-rdp-powershell-investigation.md)

Investigation of multiple failed logins followed by a successful RDP login and PowerShell execution.

**This case demonstrates:**

- Event ID 4624 / 4625 analysis;
- Logon Type 10 review;
- suspicious RDP activity investigation;
- PowerShell activity review with risky flags;
- separation of suspicious activity from confirmed incident.

---

### [Case 03: Office Malware Incident](case-studies/case-03-office-malware-incident.md)

Investigation of a Microsoft Office → PowerShell → Temp script → external connection → persistence chain.

**This case demonstrates:**

- suspicious process chain analysis;
- PowerShell abuse pattern detection;
- external connection review;
- persistence indicator identification;
- CRITICAL verdict reasoning;
- isolation and escalation recommendations.

---

## Practical Skills

### SIEM / Alert Triage

- SIEM alert review;
- detection rule logic understanding;
- alert severity assessment;
- false positive / true positive separation;
- escalation decision making;
- analyst ticket writing;
- investigation workflow: alert → evidence → verdict → action.

### Security Monitoring

- initial alert triage;
- noise / suspicious / incident classification;
- evidence-based log analysis;
- analyst verdict writing;
- next checks and recommended actions.

### Windows Security Logs

- Event ID 4624, 4625, 4634, 4688;
- successful and failed login analysis;
- Logon Type analysis;
- RDP activity investigation;
- process creation analysis;
- correlation by time and Logon ID.

More: [Windows Security Logs](skills/windows-security-logs.md)

### Sysmon

- Event ID 1: Process Create;
- Event ID 3: Network Connection;
- Event ID 11: File Create;
- ProcessGuid correlation;
- Process Create → Network Connection → File Create analysis;
- Office → PowerShell investigation scenarios.

More: [Sysmon](skills/sysmon.md)

### MITRE ATT&CK

- Execution;
- Persistence;
- Discovery;
- Lateral Movement;
- Command and Control;
- Initial Access;
- confirmed vs possible mapping.

More: [MITRE ATT&CK](skills/mitre-attck.md)

### Linux / Automation

- Linux terminal workflow;
- Git;
- Bash basics;
- Python scripting;
- PowerShell scripting;
- log parsing;
- CSV reporting;
- API integration.

More: [Linux](skills/linux.md)

---

## Current Development Focus

Current focus areas:

- SIEM fundamentals;
- detection rules;
- SOC use cases;
- alert triage;
- threat hunting basics;
- incident response workflow;
- practical investigations;
- preparation for Junior SOC / SOC L1 / Security Monitoring roles.

More: [Learning Progress](certifications/learning-progress.md)

---

## Career Objective

Seeking a Junior SOC Analyst / SOC L1 / Security Monitoring Analyst position with further development in Blue Team operations, threat detection, incident triage, and security operations.
