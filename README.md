# 📊 Latency Metrics Analyzer

![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)
![Build](https://img.shields.io/badge/build-passing-brightgreen.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

A high-performance utility for parsing system logs and identifying statistical anomalies using the Three-Sigma rule. This tool is designed for SREs and DevOps engineers who need rapid insights into system latency without heavy monitoring overhead.

---

## Overview
This tool automates the process of auditing system performance. It processes raw log files to extract latency data, identifies log levels, and flags significant performance outliers. By using mathematical standard deviations, it separates routine fluctuations from genuine system lag.

## System Workflow
The following diagram illustrates the data processing pipeline:

```mermaid
graph TD
    A[Raw Log File] --> B[Log Ingestion]
    B --> C[Field Extraction]
    C --> D[Stats Engine]
    D --> E[Mean Calculation]
    D --> F[Std Deviation]
    E & F --> G[Anomaly Detection]
    G --> H[Final Report]
- Python 3.x  
- No external dependencies

## Usage

```bash
python analyzer.py
