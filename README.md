# 🛡️ Mini-SOC with Wazuh & ELK Stack

## 📌 Overview
This project demonstrates the design and deployment of a **Mini Security Operations Center (SOC)** using **Wazuh and the ELK Stack**.
It simulates real-world cyber attacks and analyzes them using a centralized SIEM platform.

## 🧱 Architecture
- **Host Machine**: Kali Linux (Docker + Attacker)
- **Victim Machine**: Ubuntu Server 22.04
- **SOC Stack**:
  - Wazuh Manager
  - Wazuh Indexer (Elasticsearch)
  - Wazuh Dashboard (Kibana)

## ⚙️ Technologies
- Wazuh (XDR / SIEM)
- ELK Stack
- Docker & Docker Compose
- Kali Linux
- Ubuntu Server
- Apache2, OpenSSH
- Hydra, Curl, Nmap

## 🚨 Attack Scenarios
| Scenario | Description |
|--------|-------------|
| FIM | Detection of file creation, modification and deletion |
| SQL Injection | Detection via Apache access logs |
| SSH Brute Force | Correlation of failed authentication attempts |

## 📊 Results
- Real-time alerts
- Event correlation
- Threat visualization via dashboards

## 🎯 Skills Demonstrated
- SOC architecture design
- SIEM deployment
- Log analysis and correlation
- Red Team / Blue Team operations

## 👤 Author
**Youssef Mikdam**  
Cybersecurity Engineering Student
