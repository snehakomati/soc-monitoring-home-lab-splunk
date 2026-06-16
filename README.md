# soc-monitoring-home-lab-splunk
SOC Monitoring Home Lab using Splunk Enterprise and Linux Security Logs for threat detection, log analysis, and security event monitoring.
# SOC Monitoring Home Lab using Splunk & Linux Security Logs

## Project Overview

This project demonstrates the implementation of a Security Operations Center (SOC) Home Lab using Splunk Enterprise and Ubuntu Linux for security monitoring, log analysis, and threat detection.

The objective was to collect, monitor, and analyze security events from Windows and Linux systems while simulating real-world SOC analyst activities such as failed login detection, alert creation, and security event investigation.

---

## Technologies Used

* Splunk Enterprise
* Windows Event Logs
* Ubuntu Linux
* Linux Authentication Logs
* SIEM Concepts
* Security Monitoring
* Threat Detection

---

## Key Activities

### Windows Security Monitoring

* Collected Windows Security, System, and Application logs.
* Monitored authentication events using Windows Event Logs.
* Detected failed login attempts (Event ID 4625).
* Created automated alerts for suspicious authentication activity.
* Built dashboards for security event visualization.

### Linux Security Monitoring

* Analyzed Linux authentication logs (`/var/log/auth.log`).
* Investigated user login and privilege escalation events.
* Detected failed `su root` authentication attempts.
* Monitored security-related system activities.

---

## Detection Use Cases

### Failed Login Detection (Windows)

Query:

```spl
source="WinEventLog:Security" EventCode=4625
```

Purpose:
Detect failed authentication attempts and potential brute-force attacks.

### Failed Login Detection (Linux)

```bash
sudo cat /var/log/auth.log | grep -i fail
```

Purpose:
Identify authentication failures and unauthorized privilege escalation attempts.

---

## Skills Demonstrated

* SIEM Operations
* Log Analysis
* Security Monitoring
* Threat Detection
* Incident Investigation
* Alert Management
* Dashboard Creation
* Windows Security Logs
* Linux Security Logs

---

## Outcome

Successfully built a SOC monitoring environment capable of collecting, analyzing, and investigating Windows and Linux security events while simulating real-world SOC analyst workflows.
