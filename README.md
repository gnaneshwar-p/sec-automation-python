# sec-automation-python
Automates SOC tasks using Python: parses and normalizes logs, checks IP reputation via threat intelligence APIs, and analyzes phishing emails (.eml) to extract URLs, validate headers, and generate risk reports, improving workflow efficiency and security operations.
# Security Automation with Python

[![Python Version](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## Project Overview
This project demonstrates practical **SOC automation using Python**. It includes three key automation scripts designed to reduce manual effort in common Security Operations Center tasks:

1. **Log Parser** – Parses and normalizes logs from multiple sources (web servers, firewalls, Windows Event logs) into structured CSV files for analysis and SIEM ingestion.  
2. **IP Reputation Checker** – Enriches IP addresses with threat intelligence data from APIs (e.g., AbuseIPDB), automatically caching results for efficiency.  
3. **Phishing Email Analyzer** – Automatically analyzes emails (.eml format) to detect phishing indicators, extract URLs, validate headers (SPF/DKIM/DMARC), and generate risk reports.

This project highlights **hands-on skills in Python scripting, SOC automation, log analysis, threat intelligence integration, and workflow optimization** — all highly valued in cybersecurity roles.

---

## Features
- Multi-format log parsing and normalization  
- Automated IP reputation lookups with caching  
- Phishing detection using heuristic analysis and URL checks  
- JSON and CSV outputs ready for SIEM ingestion  
- CLI-driven scripts with easy configuration via environment variables  

---

## Tech Stack
- **Python 3.10+**  
- Libraries: `requests`, `pandas`, `email`, `python-dotenv`, `tqdm`  
- Threat Intelligence APIs: AbuseIPDB, VirusTotal (optional)  
- SIEM/Analysis Compatibility: Wazuh, Splunk, ELK Stack  
- Platforms: Windows, Linux, macOS  

---

## Getting Started

### 1. Clone the repository 
```bash
git clone https://github.com/<your-username>/sec-automation-python.git
cd sec-automation-python
```
---

### 2. create and activate python virtual enviroment 

```bash
python3 -m venv venv
source venv/bin/activate    # Linux/macOS
venv\Scripts\activate       # Windows
```
---
### 3. install dependencies
```bash
pip install -r requirements.txt
```
---

### 4. Add your API keys 

Create a secrets.env file with your keys:

```bash
VIRUSTOTAL_API_KEY=<your_key>
ABUSEIPDB_API_KEY=<your_key>
```
---

### 5.Run the scripts 

Log Parser
```bash
python scripts/log_parser.py --input sample_data/apache_logs.txt --output output/parsed.csv
```

IP Reputation Checker
```bash
python scripts/ip_reputation.py --input sample_data/ips.txt --output output/ip_reputation.csv
```

Phishing Email Analyzer
```bash
python scripts/phishing_analyzer.py --input sample_data/example.eml --output output/email_report.json
```
---
## Sample Output

Parsed logs: output/parsed.csv
IP reputation: output/ip_reputation.csv
Phishing report: output/email_report.json

---

## Project Highlights

Reduces manual SOC tasks by ~40% in lab environment
Demonstrates automation, scripting, and threat intelligence integration
Suitable for SOC Analyst, Security Engineer, Threat Intelligence, or Incident Response roles

---
## Next Steps / Enhancements

Integrate additional threat intelligence sources (e.g., GreyNoise, VirusTotal URL scan)
Implement HTML or dashboard visualization for phishing reports
Add multi-threading or async support for faster batch processing
Containerize with Docker for portability

---
## License

This project is licensed under the MIT License – free for personal, educational, and professional use.

---
Author

Gnaneshwar Podila
