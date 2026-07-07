# Case 01: 

## Русская версия

### Название

Легитимная активность принтера

### Severity

LOW

### Verdict

Benign activity / легитимная пользовательская активность.

### Summary

В ходе анализа была обнаружена сетевая активность, связанная с обращением пользователя к принтеру. События показывают нормальный сценарий печати: пользователь обращается к принтеру, получает ответ, устанавливает соединение и выполняет действие, похожее на обычную отправку документа на печать.

Признаков вредоносной активности, закрепления, выполнения подозрительных команд или бокового перемещения не обнаружено.

### Evidence

- User: Marina
- Activity type: Printer access
- Network interaction: Connection to printer
- Suspicious process activity: Not observed
- PowerShell activity: Not observed
- Persistence indicators: Not observed
- Lateral movement indicators: Not observed
- External suspicious IP connections: Not observed

### Analysis

Событие не содержит признаков атаки.

В данном случае отсутствуют ключевые red flags:

- нет подозрительной цепочки процессов;
- нет запуска PowerShell, cmd или других LOLBins;
- нет обращения к внешним подозрительным адресам;
- нет создания служб, задач планировщика или новых файлов в подозрительных директориях;
- нет признаков credential access, execution, persistence или lateral movement.

### MITRE ATT&CK

N/A

Активность не соответствует техникам MITRE ATT&CK, так как не обнаружено признаков вредоносного поведения.

### Final Decision

LOW / Benign.

Действий по эскалации не требуется. Событие можно закрыть как легитимную активность, если принтер действительно относится к инфраструктуре организации и пользователь имеет право им пользоваться.

### Recommended Actions

- Проверить, что устройство является корпоративным или разрешённым принтером.
- Проверить, что пользователь имеет право использовать этот принтер.
- Закрыть alert как benign, если контекст подтверждён.

---

# Case 01: 

## English Version

### Title

Legitimate Printer Activity

### Severity

LOW

### Verdict

Benign activity.

### Summary

During the investigation, network activity related to printer access was observed. The event chain matches a normal printing scenario: the user contacted a printer, received a response, established a connection, and performed an action consistent with sending a document to print.

No signs of malicious activity, persistence, suspicious command execution, or lateral movement were identified.

### Evidence

- User: Marina
- Activity type: Printer access
- Network interaction: Connection to printer
- Suspicious process activity: Not observed
- PowerShell activity: Not observed
- Persistence indicators: Not observed
- Lateral movement indicators: Not observed
- External suspicious IP connections: Not observed

### Analysis

The event does not contain signs of an attack.

In this case, no major red flags were observed:

- no suspicious process chain;
- no PowerShell, cmd, or LOLBin execution;
- no connection to suspicious external IP addresses;
- no service creation, scheduled task creation, or suspicious file creation;
- no signs of credential access, execution, persistence, or lateral movement.

### MITRE ATT&CK

N/A

The activity does not map to MITRE ATT&CK techniques because no malicious behavior was identified.

### Final Decision

LOW / Benign.

No escalation is required. The alert can be closed as benign if the printer is confirmed to be part of the organization infrastructure and the user is allowed to use it.

### Recommended Actions

- Confirm that the device is an approved corporate printer.
- Confirm that the user is allowed to access this printer.
- Close the alert as benign if the context is validated.
