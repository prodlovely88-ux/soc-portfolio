# Case 02: RDP and PowerShell Investigation

## Русская версия

### Название

Подозрительная RDP-активность с последующим запуском PowerShell

### Severity

MEDIUM

### Verdict

Подозрительная активность. Требуется проверка контекста и подтверждение легитимности действий пользователя или администратора.

### Summary

В ходе анализа была обнаружена серия неудачных попыток входа, после которых произошёл успешный вход по RDP. Далее в рамках сессии наблюдалась активность PowerShell с параметрами, которые часто требуют дополнительной проверки: `-NoProfile` и `-ExecutionPolicy Bypass`.

Также были замечены команды, похожие на Discovery-активность. Такое поведение может быть как легитимной административной работой, так и признаком компрометации учётной записи.

### Evidence

- User: alex.smirnov
- Host: WS-17
- Source IP: 10.10.5.44
- Time: 02:14 AM
- Failed logins: 12x Event ID 4625 within 5 minutes
- Successful login: 1x Event ID 4624 after failed attempts
- Logon Type: 10, RemoteInteractive / RDP
- Suspicious process: powershell.exe
- Suspicious flags:
  - `-NoProfile`
  - `-ExecutionPolicy Bypass`
- Discovery activity:
  - `whoami`
  - `hostname`
  - possible remote administration commands

### Analysis

Сама по себе RDP-сессия не является инцидентом. Однако комбинация факторов делает событие подозрительным:

- несколько неудачных попыток входа перед успешным входом;
- успешный вход по RDP ночью;
- запуск PowerShell после входа;
- использование параметров обхода execution policy;
- наличие команд, похожих на Discovery;
- необходимость проверки, является ли IP `10.10.5.44` нормальным источником для этого пользователя.

Такой сценарий может означать:

1. легитимную работу администратора;
2. ошибочные попытки входа пользователя;
3. подбор пароля с последующим успешным входом;
4. компрометацию учётной записи;
5. подготовку к дальнейшему lateral movement.

На текущем этапе недостаточно данных для классификации события как confirmed incident. Нужна дополнительная проверка контекста.

### MITRE ATT&CK

Possible mapping:

- T1021.001 - Remote Services: Remote Desktop Protocol
- T1059.001 - Command and Scripting Interpreter: PowerShell
- T1087 - Account Discovery
- T1082 - System Information Discovery

MITRE mapping указан как possible, так как активность требует подтверждения контекста.

### Next Checks

- Проверить, разрешены ли RDP-подключения для пользователя `alex.smirnov`.
- Проверить, является ли `10.10.5.44` обычным источником входа.
- Проверить географию, VPN, jump host или admin workstation.
- Проверить, были ли похожие failed logins по другим пользователям.
- Проверить команды PowerShell полностью.
- Проверить Sysmon Event ID 1 для цепочки процессов.
- Проверить Sysmon Event ID 3 на сетевые подключения после PowerShell.
- Проверить, не создавались ли новые службы, scheduled tasks или файлы в Temp/AppData.
- Проверить, были ли подключения к другим хостам после входа.

### Recommended Actions

- Не изолировать хост сразу без дополнительных признаков вредоносной активности.
- Эскалировать на дополнительную проверку, если источник входа неизвестен.
- Связаться с пользователем или администратором для подтверждения активности.
- Повысить severity до HIGH, если будут найдены признаки lateral movement, persistence или подозрительные внешние подключения.

### Final Decision

MEDIUM / Suspicious, context required.

Событие требует дополнительной проверки, но на текущем этапе не является подтверждённым инцидентом.

---

# Case 02: RDP and PowerShell Investigation

## English Version

### Title

Suspicious RDP Activity Followed by PowerShell Execution

### Severity

MEDIUM

### Verdict

Suspicious activity. Additional context is required to confirm whether the behavior was legitimate administrative activity or a possible account compromise.

### Summary

During the investigation, multiple failed login attempts were observed before a successful RDP login. After the successful login, PowerShell activity was identified with parameters commonly requiring additional review: `-NoProfile` and `-ExecutionPolicy Bypass`.

Discovery-like commands were also observed. This behavior may represent legitimate administration, but it can also indicate compromised account activity.

### Evidence

- User: alex.smirnov
- Host: WS-17
- Source IP: 10.10.5.44
- Time: 02:14 AM
- Failed logins: 12x Event ID 4625 within 5 minutes
- Successful login: 1x Event ID 4624 after failed attempts
- Logon Type: 10, RemoteInteractive / RDP
- Suspicious process: powershell.exe
- Suspicious flags:
  - `-NoProfile`
  - `-ExecutionPolicy Bypass`
- Discovery activity:
  - `whoami`
  - `hostname`
  - possible remote administration commands

### Analysis

An RDP session is not malicious by itself. However, the combination of several factors makes this activity suspicious:

- multiple failed login attempts before a successful login;
- successful RDP login during late hours;
- PowerShell execution after login;
- use of execution policy bypass parameters;
- Discovery-like commands;
- the source IP `10.10.5.44` needs to be validated as normal for this user.

This scenario may indicate:

1. legitimate administrator activity;
2. user login mistakes;
3. password guessing followed by a successful login;
4. compromised account usage;
5. preparation for further lateral movement.

At this stage, there is not enough evidence to classify the event as a confirmed incident. Additional context is required.

### MITRE ATT&CK

Possible mapping:

- T1021.001 - Remote Services: Remote Desktop Protocol
- T1059.001 - Command and Scripting Interpreter: PowerShell
- T1087 - Account Discovery
- T1082 - System Information Discovery

MITRE mapping is listed as possible because the activity requires context validation.

### Next Checks

- Confirm whether RDP access is expected for `alex.smirnov`.
- Verify whether `10.10.5.44` is a normal source IP for this user.
- Check whether the source is a VPN, jump host, or admin workstation.
- Look for similar failed login attempts against other accounts.
- Review the full PowerShell command line.
- Check Sysmon Event ID 1 for process chain details.
- Check Sysmon Event ID 3 for network connections after PowerShell execution.
- Check for new services, scheduled tasks, or suspicious files in Temp/AppData.
- Check whether the host connected to other internal systems after login.

### Recommended Actions

- Do not isolate the host immediately without additional malicious indicators.
- Escalate for further review if the source IP is unknown.
- Contact the user or administrator to validate the activity.
- Increase severity to HIGH if lateral movement, persistence, or suspicious external connections are confirmed.

### Final Decision

MEDIUM / Suspicious, context required.

The event requires further investigation, but it is not a confirmed incident at this stage.
