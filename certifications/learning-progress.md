# Learning Progress

## Русская версия

## SOC / Blue Team Training Progress

Этот раздел фиксирует практический прогресс в изучении направлений SOC, Blue Team, анализа логов и расследования инцидентов.

Основной подход: не только изучение теории, но и регулярная практика на сценариях, логах, Event ID, Sysmon-событиях, кейсах расследований и собственных инструментах автоматизации.

---

## Изученные направления

### Network Fundamentals

Изучены базовые темы, необходимые для анализа сетевой активности:

- OSI / TCP-IP
- TCP и UDP
- DNS
- DHCP
- HTTP / HTTPS
- базовые сетевые порты
- ping
- traceroute
- nslookup
- dig
- curl
- whois

Практический фокус:

- понимание сетевых соединений;
- анализ базовой сетевой активности;
- различие нормального и подозрительного сетевого поведения;
- подготовка к анализу сетевых событий в SIEM.

---

### Linux Basics for Security

Изучены базовые Linux-навыки, необходимые для работы с логами, файлами, правами доступа и терминалом.

Практически отработано:

- навигация по файловой системе;
- работа с `/etc`, `/var/log`, `/home`, `/tmp`;
- `chmod`;
- `chown`;
- `find`;
- `grep`;
- базовый Bash;
- поиск файлов с опасными правами;
- фильтрация логов;
- работа с Git.

Практический фокус:

- анализ файлов и логов;
- понимание прав доступа;
- работа с терминалом как основной рабочей средой;
- подготовка к задачам SOC и системного анализа.

---

### Windows Security Logs

Изучены и отработаны базовые события Windows Security Logs:

- `4624` - Successful Logon
- `4625` - Failed Logon
- `4634` - Logoff
- `4688` - Process Creation

Практически отработано:

- анализ успешных и неуспешных входов;
- разбор Logon Type;
- RDP Logon Type 10;
- локальные входы;
- service logon;
- анализ пользователей, хостов и Source IP;
- корреляция событий по времени и Logon ID;
- анализ создания процессов;
- подозрительные цепочки процессов;
- PowerShell triage.

Практический фокус:

- определить, является ли событие шумом, подозрительной активностью или инцидентом;
- отличать нормальную административную активность от возможной компрометации;
- строить понятный analyst verdict.

---

### Sysmon

Изучены и отработаны базовые события Sysmon:

- `Sysmon Event ID 1` - Process Create
- `Sysmon Event ID 3` - Network Connection
- `Sysmon Event ID 11` - File Create

Практически отработано:

- анализ создания процессов;
- анализ сетевых подключений процессов;
- анализ создания файлов;
- корреляция событий по ProcessGuid;
- связка Process Create → Network Connection → File Create;
- анализ подозрительных директорий:
  - Temp
  - AppData
  - Downloads
  - Public
- проверка подозрительных запусков PowerShell;
- анализ Office → PowerShell сценариев.

Практический фокус:

- расследование подозрительной активности на Windows-хосте;
- выявление цепочек выполнения;
- подготовка к triage в SIEM.

---

### MITRE ATT&CK

Изучены базовые тактики и техники, применимые к SOC-расследованиям.

Основной фокус:

- Initial Access
- Execution
- Persistence
- Discovery
- Lateral Movement
- Command and Control

Практически отработаны техники:

- `T1059.001` - PowerShell
- `T1021.001` - Remote Desktop Protocol
- `T1087` - Account Discovery
- `T1082` - System Information Discovery
- `T1053.005` - Scheduled Task
- `T1543.003` - Windows Service
- `T1071.001` - Web Protocols
- `T1566.001` - Spearphishing Attachment

Практический фокус:

- не фантазировать MITRE mapping без подтверждения;
- разделять confirmed и possible mapping;
- использовать MITRE как язык описания активности, а не как украшение отчёта.

---

### SOC Case Reporting

Практически отработан формат incident report / analyst ticket:

- Title
- Summary
- Severity
- Verdict
- Evidence
- Analysis / Why
- MITRE ATT&CK
- Next Checks
- Recommended Actions
- Final Decision

Практический фокус:

- Evidence = факты из логов;
- Analysis = объяснение, почему это важно;
- Verdict = итоговая оценка;
- Actions = что делать дальше.


### SIEM Fundamentals / Alert Triage

Практически отработано:

- структура SIEM alert;
- связь event → alert → incident;
- detection rule logic;
- use case thinking;
- severity assessment;
- false positive / true positive logic;
- escalation decision making;
- analyst ticket writing;
- разбор suspicious и confirmed incident сценариев.

Практические сценарии:

- multiple failed RDP logins followed by successful login;
- suspicious PowerShell after Office document;
- Office → PowerShell → Temp script → external connection → persistence;
- benign printer activity;
- suspicious admin-like RDP and PowerShell activity.

Практический фокус:

- не паниковать по одному red flag;
- собирать цепочку evidence;
- отделять suspicious activity от confirmed incident;
- выбирать действия по severity;
- писать понятный analyst ticket на английском.


---

## Практические проекты

### Windows Security Log Triage

PowerShell-инструмент для анализа Windows Event ID 4688 и выявления подозрительной активности процессов.

### IOC Log Enricher

Python-инструмент для извлечения публичных IP-адресов из логов, контекстного triage и AbuseIPDB enrichment.

---

## Текущий фокус развития

В настоящий момент продолжается развитие в направлениях:

- SIEM fundamentals;
- detection rules;
- use cases;
- alert triage;
- threat hunting basics;
- practical SOC investigations;
- портфолио для Junior SOC / SOC L1 / Security Monitoring ролей.

---

## English Version

## SOC / Blue Team Training Progress

This section documents my practical progress in SOC, Blue Team, log analysis, and incident investigation.

The main approach is practice-oriented: working with realistic scenarios, logs, Event IDs, Sysmon events, investigation cases, and custom automation tools.

---

## Covered Areas

### Network Fundamentals

Covered topics:

- OSI / TCP-IP
- TCP and UDP
- DNS
- DHCP
- HTTP / HTTPS
- common network ports
- ping
- traceroute
- nslookup
- dig
- curl
- whois

Practical focus:

- understanding network connections;
- analyzing basic network activity;
- distinguishing normal and suspicious network behavior;
- preparing for network event analysis in SIEM.

---

### Linux Basics for Security

Covered Linux skills required for log analysis, file handling, permissions, and terminal-based workflows.

Practiced areas:

- filesystem navigation;
- working with `/etc`, `/var/log`, `/home`, `/tmp`;
- `chmod`;
- `chown`;
- `find`;
- `grep`;
- basic Bash;
- searching for risky file permissions;
- log filtering;
- Git workflow.

Practical focus:

- file and log analysis;
- understanding permissions;
- using terminal as the main working environment;
- preparing for SOC and system analysis tasks.

---

### Windows Security Logs

Covered core Windows Security Logs:

- `4624` - Successful Logon
- `4625` - Failed Logon
- `4634` - Logoff
- `4688` - Process Creation

Practiced areas:

- successful and failed login analysis;
- Logon Type analysis;
- RDP Logon Type 10;
- local logons;
- service logons;
- user, host, and Source IP analysis;
- correlation by time and Logon ID;
- process creation analysis;
- suspicious process chains;
- PowerShell triage.

Practical focus:

- determining whether an event is noise, suspicious activity, or an incident;
- distinguishing normal administrative activity from possible compromise;
- building clear analyst verdicts.

---

### Sysmon

Covered core Sysmon events:

- `Sysmon Event ID 1` - Process Create
- `Sysmon Event ID 3` - Network Connection
- `Sysmon Event ID 11` - File Create

Practiced areas:

- process creation analysis;
- process network connection analysis;
- file creation analysis;
- correlation by ProcessGuid;
- Process Create → Network Connection → File Create correlation;
- suspicious directory analysis:
  - Temp
  - AppData
  - Downloads
  - Public
- suspicious PowerShell execution review;
- Office → PowerShell scenario analysis.

Practical focus:

- investigating suspicious activity on Windows hosts;
- identifying execution chains;
- preparing for SIEM-based triage.

---

### MITRE ATT&CK

Covered basic tactics and techniques relevant to SOC investigations.

Main focus areas:

- Initial Access
- Execution
- Persistence
- Discovery
- Lateral Movement
- Command and Control

Practiced techniques:

- `T1059.001` - PowerShell
- `T1021.001` - Remote Desktop Protocol
- `T1087` - Account Discovery
- `T1082` - System Information Discovery
- `T1053.005` - Scheduled Task
- `T1543.003` - Windows Service
- `T1071.001` - Web Protocols
- `T1566.001` - Spearphishing Attachment

Practical focus:

- avoiding unsupported MITRE mapping;
- separating confirmed and possible mappings;
- using MITRE as an investigation language, not decoration.

---

### SOC Case Reporting

Practiced incident report / analyst ticket structure:

- Title
- Summary
- Severity
- Verdict
- Evidence
- Analysis / Why
- MITRE ATT&CK
- Next Checks
- Recommended Actions
- Final Decision

Practical focus:

- Evidence = facts from logs;
- Analysis = explanation of why the facts matter;
- Verdict = final assessment;
- Actions = what should be done next.

### SIEM Fundamentals / Alert Triage

Practiced areas:

- SIEM alert structure;
- event → alert → incident workflow;
- detection rule logic;
- SOC use case thinking;
- severity assessment;
- false positive / true positive logic;
- escalation decision making;
- analyst ticket writing;
- suspicious vs confirmed incident separation.

Practical scenarios:

- multiple failed RDP logins followed by successful login;
- suspicious PowerShell after Office document;
- Office → PowerShell → Temp script → external connection → persistence;
- benign printer activity;
- suspicious admin-like RDP and PowerShell activity.

Practical focus:

- avoiding overreaction to a single red flag;
- collecting evidence chains;
- separating suspicious activity from confirmed incidents;
- choosing actions based on severity;
- writing clear analyst tickets in English.

---

## Practical Projects

### Windows Security Log Triage

A PowerShell-based tool for analyzing Windows Event ID 4688 and identifying suspicious process activity.

### IOC Log Enricher

A Python-based tool for extracting public IP addresses from logs, performing context-aware triage, and enriching results with AbuseIPDB.

---

## Current Development Focus

Currently expanding practical knowledge in:

- SIEM fundamentals;
- detection rules;
- use cases;
- alert triage;
- threat hunting basics;
- practical SOC investigations;
- portfolio preparation for Junior SOC / SOC L1 / Security Monitoring roles.
