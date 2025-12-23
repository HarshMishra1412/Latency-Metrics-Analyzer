# 📊 Latency Metrics Analyzer

![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)
![Build](https://img.shields.io/badge/build-passing-brightgreen.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

A high-performance utility for parsing system logs and identifying statistical anomalies using the Three-Sigma rule.

---

## Overview
This tool automates system performance auditing by extracting latency data and flagging significant outliers using mathematical standard deviations. It helps in separating routine fluctuations from genuine system lag.

## System Architecture
```text
[ Raw Logs ] --> [ Regex Parser ] --> [ Statistics Engine ]
                                             |
                                     -----------------
                                     |               |
                              [ Mean/Std Dev ] [ Anomaly Detection ]
                                     |               |
                                     -----------------
                                             |
                                     [ Final Performance Report ]
- Python 3.x  
- No external dependencies

## Usage

```bash
python analyzer.py
