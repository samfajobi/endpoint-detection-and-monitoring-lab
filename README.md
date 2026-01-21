# Wazuh Windows Endpoint Monitoring Lab

This project demonstrates **Windows endpoint security monitoring using Wazuh**, showcasing two common real-world approaches used in SOC environments:

1. **Baseline monitoring using native Windows Event Logs**
2. **Enhanced monitoring using Sysmon integrated with Wazuh**

The goal is to highlight the **difference in visibility, detection capability, and SOC response maturity** between environments that can and cannot deploy Sysmon.

---

## 🎯 Objectives
- Demonstrate practical Windows endpoint monitoring with Wazuh
- Compare detection capabilities with and without Sysmon
- Simulate SOC alerting, investigation, and response workflows
- Map detections to MITRE ATT&CK techniques
- Document playbooks for common endpoint threats

---

## 🏗️ Architecture Overview

| Component | Description |
|---------|------------|
| Wazuh Manager | Central log analysis and correlation |
| Wazuh Indexer | Storage and search of security events |
| Wazuh Dashboard | Visualization and SOC investigation |
| Windows Endpoint | Monitored host (with or without Sysmon) |

📌 Two monitoring profiles are implemented to reflect real enterprise constraints.

---

## 🔍 Monitoring Profiles

### 1️⃣ Profile A: Windows Event Logs Only (No Sysmon)
- Uses native Windows Security, System, and Application logs
- Suitable for restricted or legacy environments
- Provides baseline detection and visibility

### 2️⃣ Profile B: Windows Event Logs + Sysmon
- Sysmon installed and configured on the endpoint
- Provides enhanced telemetry (process, network, registry)
- Enables advanced threat detection and correlation

---

## 📊 Detection Comparison Summary

| Capability | Without Sysmon | With Sysmon |
|----------|---------------|------------|
| Process creation visibility | Limited | Full |
| Network connection tracking | Limited | Detailed |
| Registry monitoring | Minimal | Extensive |
| Threat detection depth | Baseline | Advanced |
| SOC investigation quality | Moderate | High |

---

## 🧠 SOC Use Case
This lab simulates how a SOC:
- Detects suspicious endpoint activity
- Investigates alerts using Wazuh
- Applies playbooks for response
- Understands detection gaps and trade-offs

---

## 📁 Repository Structure
See folder layout below for implementation details.
