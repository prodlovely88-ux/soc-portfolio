# Windows Security Logs

## Русская версия

Работаю с базовыми событиями Windows Security Logs,  для анализа входов, активности пользователей и создания процессов.

## Ключевые Event ID в мониторинге

- `4624` - Successful Logon
- `4625` - Failed Logon
- `4634` - Logoff
- `4688` - Process Creation
- `4698` - Scheduled Task Created

## Практические навыки

- Анализ успешных и неуспешных попыток входа
- Разбор Logon Type
- Выявление подозрительной RDP-активности
- Анализ процесса, пользователя и командной строки
- Корреляция событий по времени и Logon ID
- Первичный triage подозрительных событий
- Проверка scheduled task creation как возможного persistence indicator
- Корреляция логинов, process creation и persistence events

## Примеры сценариев

- Multiple failed logins followed by successful login
- RDP login outside normal working hours
- PowerShell execution after interactive login
- Suspicious process creation with unusual command-line flags

---

# Windows Security Logs

## English Version

I work with core Windows Security Logs for login analysis, user activity investigation, and process creation monitoring.

## Core Event IDs

- `4624` - Successful Logon
- `4625` - Failed Logon
- `4634` - Logoff
- `4688` - Process Creation
- `4698` - Scheduled Task Created

## Practical Skills

- Successful and failed login analysis
- Logon Type analysis
- Suspicious RDP activity investigation
- Process, user, and command-line analysis
- Event correlation by time and Logon ID
- Initial suspicious event triage
- Scheduled task creation review as a possible persistence indicator
- Correlation of logon, process creation, and persistence events

## Example Scenarios

- Multiple failed logins followed by successful login
- RDP login outside normal working hours
- PowerShell execution after interactive login
- Suspicious process creation with unusual command-line flags
