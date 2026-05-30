# Windows Security Logs

## Русская версия

Работаю с базовыми событиями Windows Security Logs, которые используются в SOC для анализа входов, активности пользователей и создания процессов.

## Изученные Event ID

- `4624` - Successful Logon
- `4625` - Failed Logon
- `4634` - Logoff
- `4688` - Process Creation

## Практические навыки

- Анализ успешных и неуспешных попыток входа
- Разбор Logon Type
- Выявление подозрительной RDP-активности
- Анализ процесса, пользователя и командной строки
- Корреляция событий по времени и Logon ID
- Первичный triage подозрительных событий

## Примеры сценариев

- Multiple failed logins followed by successful login
- RDP login outside normal working hours
- PowerShell execution after interactive login
- Suspicious process creation with unusual command-line flags

---

# Windows Security Logs

## English Version

I work with core Windows Security Logs used in SOC environments for login analysis, user activity investigation, and process creation monitoring.

## Covered Event IDs

- `4624` - Successful Logon
- `4625` - Failed Logon
- `4634` - Logoff
- `4688` - Process Creation

## Practical Skills

- Successful and failed login analysis
- Logon Type analysis
- Suspicious RDP activity investigation
- Process, user, and command-line analysis
- Event correlation by time and Logon ID
- Initial suspicious event triage

## Example Scenarios

- Multiple failed logins followed by successful login
- RDP login outside normal working hours
- PowerShell execution after interactive login
- Suspicious process creation with unusual command-line flags
