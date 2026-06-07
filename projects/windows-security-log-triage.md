
# Windows Security Log Triage

## Описание

Windows Security Log Triage - это учебный SOC-инструмент для анализа событий создания процессов в Windows Security Logs, в первую очередь Event ID 4688.

Проект предназначен для первичного triage подозрительной активности, анализа цепочек процессов и выявления типовых признаков злоупотребления PowerShell.

## Цель проекта

Цель проекта - ускорить первичный анализ событий Windows Event ID 4688 и выделить события, которые требуют внимания аналитика.

Основной фокус:

- анализ создания процессов;
- выявление подозрительных параметров PowerShell;
- анализ цепочек Parent Process → Child Process;
- обнаружение команд Discovery;
- формирование отчёта для дальнейшего расследования.

## Реализованные возможности

- Парсинг событий Windows Security Event ID 4688
- Извлечение времени, пользователя, процесса, родительского процесса и командной строки
- Обнаружение подозрительных флагов PowerShell:
  - `-NoProfile`
  - `-ExecutionPolicy Bypass`
  - `-EncodedCommand`
  - `-WindowStyle Hidden`
- Выявление Discovery-команд:
  - `whoami`
  - `hostname`
  - `ipconfig`
  - `net user`
  - `net group`
- Поддержка suspicious-only фильтрации
- Формирование CSV-отчёта
- Добавление verdict, severity, reason и triage note

## Что демонстрирует проект

Проект показывает практические навыки в следующих областях:

- Windows Security Logs
- Event ID 4688
- Process Creation Analysis
- PowerShell triage
- Parent-child process correlation
- Suspicious command detection
- SOC analyst workflow
- PowerShell scripting
- SIEM-style alert triage thinking
- Severity and verdict assignment
- Analyst-friendly report structure
- Detection logic based on process behavior

## Пример сценария

Подозрительная цепочка:

explorer.exe → powershell.exe
CommandLine: powershell.exe -NoProfile -ExecutionPolicy Bypass

Такой запуск не всегда является вредоносным, но требует проверки контекста, так как похожие параметры часто используются для обхода политик выполнения и запуска подозрительных скриптов.

## Возможные улучшения

- Добавить корреляцию Event ID 4624/4625 с запуском процессов
- Добавить Sysmon Event ID 1 / 3 / 11 поддержку
- Добавить Event ID 4698 для scheduled task persistence
- Добавить JSON export
- Добавить HTML report
- Добавить MITRE ATT&CK mapping


GitHub Repo: https://github.com/prodlovely88-ux/windows-security-log-triage

Windows Security Log Triage
Description

Windows Security Log Triage is a practical SOC-focused tool for analyzing Windows process creation events, primarily Windows Security Event ID 4688.

The project is designed to support initial triage of suspicious activity, process chain analysis, and detection of common PowerShell abuse patterns.

Project Goal

The goal of this project is to speed up initial analysis of Windows Event ID 4688 and highlight events that require analyst attention.

Main focus areas:

process creation analysis;
suspicious PowerShell flag detection;
Parent Process → Child Process analysis;
Discovery command detection;
report generation for further investigation.
Implemented Features
Windows Security Event ID 4688 parsing
Extraction of timestamp, user, process, parent process, and command line
Detection of suspicious PowerShell flags:
-NoProfile
-ExecutionPolicy Bypass
-EncodedCommand
-WindowStyle Hidden
Discovery command identification:
whoami
hostname
ipconfig
net user
net group
Suspicious-only filtering
CSV report generation
Verdict, severity, reason, and triage note fields
Skills Demonstrated

This project demonstrates practical skills in:

Windows Security Logs
Event ID 4688
Process Creation Analysis
PowerShell triage
Parent-child process correlation
Suspicious command detection
SOC analyst workflow
PowerShell scripting
Example Scenario

Suspicious process chain:

explorer.exe → powershell.exe
CommandLine: powershell.exe -NoProfile -ExecutionPolicy Bypass

This behavior is not always malicious, but it requires context validation because these parameters are often used to bypass execution policies and run suspicious scripts.

Future Improvements
Add Event ID 4624/4625 correlation
Add Sysmon Event ID 1 support
Add JSON export
Add MITRE ATT&CK mapping
Add HTML reporting
Repository

GitHub: https://github.com/prodlovely88-ux/windows-security-log-triage
