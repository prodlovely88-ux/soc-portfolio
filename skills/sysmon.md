# Sysmon

## Русская версия

Использую Sysmon для более детального анализа активности процессов, сетевых подключений и создания файлов на Windows-хостах.

## Ключевые Event ID в мониторинге

- `Sysmon Event ID 1` - Process Create
- `Sysmon Event ID 3` - Network Connection
- `Sysmon Event ID 11` - File Create

## Практические навыки

- Анализ цепочек процессов
- Корреляция событий по ProcessGuid
- Поиск подозрительных запусков PowerShell
- Анализ сетевых подключений процессов
- Проверка создания файлов в Temp, AppData и других подозрительных директориях
- Связка Process Create → Network Connection → File Create

## Примеры сценариев

- PowerShell launched from Office process
- Script created in user Temp directory
- Process connection to external IP address
- Correlation of process, network, and file creation events

---

# Sysmon

## English Version

I use Sysmon for deeper analysis of process activity, network connections, and file creation events on Windows hosts.

## Core Event IDs

- `Sysmon Event ID 1` - Process Create
- `Sysmon Event ID 3` - Network Connection
- `Sysmon Event ID 11` - File Create

## Practical Skills

- Process chain analysis
- Event correlation by ProcessGuid
- Suspicious PowerShell execution detection
- Process network connection analysis
- File creation analysis in Temp, AppData, and other suspicious directories
- Correlation of Process Create → Network Connection → File Create

## Example Scenarios

- PowerShell launched from an Office process
- Script created in user Temp directory
- Process connection to an external IP address
- Correlation of process, network, and file creation events
