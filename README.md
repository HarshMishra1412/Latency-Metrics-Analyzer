# 📊 Latency Metrics Analyzer

![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Build](https://img.shields.io/badge/build-passing-brightgreen.svg)
![Platform](https://img.shields.io/badge/platform-linux%20%7C%20macos%20%7C%20windows-lightgrey.svg)

A professional Python-based utility for parsing system log files, aggregating latency metrics, and identifying anomalously slow events using statistical thresholds.

---

##  Overview

**Latency Metrics Analyzer** helps DevOps and SREs quickly summarize system behavior without complex monitoring stacks. It transforms raw, messy log data into actionable performance insights by automating the detection of system bottlenecks.

---

## Key Features

- **Smart Parsing:** Automatically extracts latency values from structured log entries using optimized regex.
- **Log Level Analysis:** Provides precise counts for INFO, WARN, and ERROR events to gauge system health.
- **Statistical Anomalies:** Uses the $mean + 3\sigma$ (Three-Sigma) rule to flag unusually slow requests.
- **Performance Profiling:** Reports the Top N slowest latencies for deep-dive root-cause analysis.
- **Zero Dependencies:** Built entirely using Python's standard library for maximum portability.

---

## Final Report Key Features

The analyzer generates a structured terminal report that provides a 360-degree view of your system's performance. Key components include:

- **Baseline Metrics Summary:** Displays the total logs processed alongside the calculated Average ($\mu$) and Median latency to establish a clear performance baseline.
- **Dynamic Threshold Identification:** Explicitly states the calculated Anomaly Threshold. This helps engineers understand exactly where "normal" ends and "slow" begins for their specific environment.
- **Anomaly Breakdown:** A detailed list of events that breached the $3\sigma$ limit, including timestamps and specific endpoints, allowing for immediate troubleshooting.
- **Severity Distribution:** A tabular breakdown of log levels (INFO, WARN, ERROR) to help correlate latency spikes with system errors.
- **Worst-Case Ranking:** An isolated view of the absolute slowest requests (Top N), ensuring that the most critical performance issues are addressed first.

---

## How It Works

The tool processes logs through a highly efficient pipeline:

1. **Stream Reading:** Reads logs line-by-line to maintain a low memory footprint even with large files.
2. **Data Extraction:** Parses each entry into structured fields for mathematical processing.
3. **Statistical Modeling:** Computes the average and standard deviation to establish a dynamic "normal" range.
4. **Flagging:** Identifies outliers where:
   $$\text{Latency} > (\mu + 3\sigma)$$



---

## Project Structure

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

