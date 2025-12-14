

## 🚀 Implementation Steps

### Step 1️⃣ Install Sysmon on Windows

Install Sysmon using a configuration file:

```powershell
Sysmon64.exe -i sysmon-config.xml
```

Verify the service is running:

```powershell
Get-Service Sysmon64
```

---

### Step 2️⃣ Install Wazuh Agent

1. Download the **Wazuh Agent for Windows**
2. Register the agent with the **Wazuh Manager**
3. Start the agent service

Verify agent status:

```powershell
net start wazuh
```

---

### Step 3️⃣ Configure Log Collection

Configure the Wazuh Agent to collect:

* Sysmon logs
* Windows Security logs

Sysmon event log source:

```text
Microsoft-Windows-Sysmon/Operational
```

---

### Step 4️⃣ Detection and Alerting

Wazuh detection rules can identify:

* Suspicious PowerShell execution
* Credential dumping attempts
* Malware execution patterns
* Abnormal outbound network connections

All alerts are visible in the **Wazuh Dashboard**.

---

## 🔎 Example Detection Scenarios

* PowerShell execution with encoded commands
* Office applications spawning child processes
* Outbound connections from uncommon binaries
* Registry-based persistence techniques

---

## 🎯 SOC Use Cases

This project supports:

* Endpoint threat detection
* Incident investigation
* Malware analysis
* Threat hunting
* Compliance monitoring

---

## 🧠 Key Takeaway

> **Sysmon provides visibility.
> Wazuh provides intelligence.**

Together, they deliver powerful **endpoint monitoring and detection** comparable to commercial EDR solutions.

---

## 📚 Future Improvements

* Integrate alerts with SIEM (Splunk / Elastic)
* Map detections to MITRE ATT&CK
* Create custom Sysmon and Wazuh rules
* Automate response actions

---

## 👤 Author

**Olusegun Fajobi**
Cybersecurity Engineer (Blue & Red Team)
GitHub: [https://github.com/samfajobi](https://github.com/samfajobi)

```

---

If you want next, I can:
- 🔥 Add **screenshots sections** (very good for GitHub)
- 🔥 Add **MITRE ATT&CK mapping table**
- 🔥 Turn this into a **portfolio-ready SOC project**
- 🔥 Add **custom Sysmon + Wazuh detection examples**

Just say the word 👊
```
