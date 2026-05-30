# IOC Log Enricher

## Описание

IOC Log Enricher - это Python-инструмент для извлечения публичных IPv4-адресов из логов, контекстного анализа найденных индикаторов и обогащения данных через AbuseIPDB.

Проект предназначен для базового triage индикаторов компрометации и формирования понятного отчёта для SOC-аналитика.

## Цель проекта

Цель проекта - автоматизировать первичный анализ IP-адресов в логах и помочь аналитику быстрее определить, какие индикаторы требуют внимания.

Основной фокус:

- извлечение IP-адресов из логов;
- фильтрация private/local/reserved адресов;
- подсчёт повторений индикаторов;
- анализ контекста строк;
- обогащение через AbuseIPDB;
- экспорт отчёта в CSV.

## Реализованные возможности

- Извлечение IPv4-адресов из лог-файлов
- Валидация IP через стандартный модуль `ipaddress`
- Фильтрация приватных, локальных и зарезервированных адресов
- Подсчёт количества повторений каждого IP
- Контекстный анализ строк логов
- Присвоение verdict:
  - `HIGH`
  - `SUSPICIOUS`
  - `CHECK`
  - `INFO`
- Интеграция с AbuseIPDB
- Поддержка `.env` для API-ключа
- Консольный отчёт в человекочитаемом формате
- Экспорт результата в CSV

## Что демонстрирует проект

Проект показывает практические навыки в следующих областях:

- Python scripting
- Log analysis
- IOC extraction
- Threat Intelligence
- AbuseIPDB API integration
- CSV reporting
- Context-aware triage
- Secure handling of API keys

## Пример сценария

Лог содержит несколько неудачных попыток входа с публичного IP-адреса.

Инструмент:

1. извлекает IP;
2. проверяет, является ли он публичным;
3. считает количество повторений;
4. анализирует контекст строки;
5. запрашивает репутацию в AbuseIPDB;
6. формирует итоговый verdict.

Пример вывода:
IP: 185.220.101.1
Verdict: SUSPICIOUS
Reason: Failed login context and high AbuseIPDB score
Важный аналитический вывод

Репутация IP сама по себе не является финальным доказательством атаки.

Корректный triage должен учитывать:

локальный контекст события;
количество повторений;
тип активности;
внешний reputation score;
источник логов;
поведение пользователя или хоста.
Возможные улучшения
Добавить VirusTotal enrichment
Добавить поддержку доменов и URL
Добавить JSON export
Добавить HTML-отчёт
Добавить severity scoring
Добавить unit tests
Репозиторий

#GitHub: https://github.com/prodlovely88-ux/ioc-log-enricher

## English version

#IOC Log Enricher

#Description

IOC Log Enricher is a Python-based tool for extracting public IPv4 addresses from logs, performing context-aware indicator triage, and enriching results with AbuseIPDB reputation data.

The project is designed to support initial IOC triage and generate clear reports for SOC analysis.

#Project Goal

The goal of this project is to automate initial IP address analysis in logs and help analysts identify indicators that require attention.

#Main focus areas:

IP address extraction from logs;
filtering private, local, and reserved addresses;
indicator frequency counting;
log line context analysis;
AbuseIPDB enrichment;
CSV report export.

#Implemented Features

IPv4 extraction from log files
IP validation using the Python ipaddress module
Filtering of private, local, and reserved addresses
Count aggregation per IP address
Log line context analysis

#Verdict assignment:
HIGH
SUSPICIOUS
CHECK
INFO
AbuseIPDB integration
.env support for API key handling
Human-readable console report
CSV export
Skills Demonstrated

#This project demonstrates practical skills in:

Python scripting
Log analysis
IOC extraction
Threat Intelligence
AbuseIPDB API integration
CSV reporting
Context-aware triage
Secure handling of API keys
Example Scenario

A log file contains multiple failed login attempts from a public IP address.

#The tool:

extracts the IP address;
validates that it is public;
counts occurrences;
analyzes log line context;
requests AbuseIPDB reputation data;
generates a final verdict.

#Example output:

IP: 185.220.101.1
Verdict: SUSPICIOUS
Reason: Failed login context and high AbuseIPDB score
Important Analytical Note

IP reputation alone is not final proof of malicious activity.

Proper triage should consider:

local event context;
number of occurrences;
activity type;
external reputation score;
log source;
user or host behavior.
Future Improvements
Add VirusTotal enrichment
Add domain and URL support
Add JSON export
Add HTML reporting
Add severity scoring
Add unit tests
Repository

#GitHub: https://github.com/prodlovely88-ux/ioc-log-enricher
