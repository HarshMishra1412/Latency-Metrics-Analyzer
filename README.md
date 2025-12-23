# 📊 Latency Metrics Analyzer

![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Build](https://img.shields.io/badge/build-passing-brightgreen.svg)
![Platform](https://img.shields.io/badge/platform-linux%20%7C%20macos%20%7C%20windows-lightgrey.svg)

A professional Python-based utility for parsing system log files, aggregating latency metrics, and identifying anomalously slow events using statistical thresholds.

---

## 🎯 Overview

**Latency Metrics Analyzer** helps DevOps and SREs quickly summarize system behavior without complex monitoring stacks. It transforms raw, messy log data into actionable performance insights.

### ✨ Key Features
- **Smart Parsing:** Automatically extracts latency values from structured log entries.
- **Log Level Analysis:** Provides counts for `INFO`, `WARN`, and `ERROR` events.
- **Statistical Anomalies:** Uses the $mean + 3\sigma$ (Three-Sigma) rule to flag unusually slow requests.
- **Performance Profiling:** Reports the Top N slowest latencies for root-cause analysis.
- **Zero Dependencies:** Built entirely using Python's standard library.

---

## ⚙️ How It Works

The tool processes logs through a highly efficient pipeline:

1. **Stream Reading:** Reads logs line-by-line to maintain a low memory footprint.
2. **Data Extraction:** Parses each entry into structured fields.
3. **Statistical Modeling:** Computes the average and standard deviation to establish a dynamic "normal" range.
4. **Flagging:** Identifies outliers where:
   $$\text{Latency} > (\mu + 3\sigma)$$

---

## 📂 Project Structure

```text
latency-metrics-analyzer/
├── log_parser.py    # Logic for reading and cleaning log data
├── stats_log.py     # Core statistical engine and CLI entry point
├── sample.log       # Sample log file for testing
└── README.md        # Documentation
## Requirements

- Python 3.x  
- No external dependencies

## Usage

```bash
python analyzer.py
