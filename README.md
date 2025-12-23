# latency-metrics-analyzer

A Python-based utility for parsing system log files, aggregating latency metrics, and identifying anomalously slow events using simple statistical thresholds.

## What it does

This tool reads structured system logs and produces a concise summary of system behavior by:

- Extracting latency values from log entries  
- Counting INFO, WARN, and ERROR events  
- Computing average latency and anomaly thresholds  
- Flagging unusually slow requests  
- Reporting the top N slowest latencies  

The goal is to summarize what is happening in the system, not to diagnose root causes or predict failures.

## How it works

- Logs are read line by line from a text file  
- Each entry is parsed into structured fields  
- Latency metrics are aggregated  
- Anomalies are detected using a mean + 3σ statistical threshold  

All analysis is performed locally using Python’s standard library.

## Project structure

```text
latency-metrics-analyzer/
├── log_parser.py
├── stats_log.py
├── sample.log
└── README.md
```

## Requirements

- Python 3.x  
- No external dependencies

## Usage

```bash
python analyzer.py
