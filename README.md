# CSA Hands-On Cybersecurity Lab Portfolio

Hands-on cybersecurity labs and practical exercises completed during EC-Council Certified SOC Analyst (CSA) training.

This repository documents my practical work across security monitoring, network analysis, SIEM operations, threat detection, endpoint security, threat hunting, malware analysis, and incident response.

## Training Areas

- Linux and Kali Linux Administration
- Networking Fundamentals
- Wireshark Packet Analysis
- Network Reconnaissance and Port Scanning
- Controlled Security Testing Labs
- Linux Firewall and Security Logging
- Snort IDS/IPS
- Windows Event Logs and Sysmon
- SIEM Operations with IBM QRadar
- SIEM Operations with Splunk
- Threat Intelligence
- Threat Hunting
- Malware Analysis
- YARA Detection Rules
- Wazuh Endpoint Monitoring and File Integrity Monitoring
- Incident Response
- Jira and SOAR Concepts

## Security Tools Used

- Kali Linux
- IBM QRadar
- Splunk
- Wazuh
- Wireshark
- Snort
- Sysmon
- Nmap
- Metasploit
- YARA
- VirusTotal
- AbuseIPDB
- Hydra
- Medusa
- SQLMap
- DIRB
- hping3
- Netcat
- iptables
- Jira

## Key Practical Work

### SIEM and Log Analysis

- Configured and worked with IBM QRadar Community Edition.
- Ingested Linux security logs into QRadar using rsyslog.
- Investigated authentication failures and successful logins.
- Practiced QRadar AQL searches and event/flow analysis.
- Created detection rules and investigated generated offenses.
- Performed false-positive tuning.
- Built QRadar dashboards and reports.
- Ingested Apache, SSH, Windows, and firewall logs into Splunk.
- Practiced SPL-based log analysis, filtering, deduplication, statistics, and visualization.
- Created Splunk alerts for directory brute-force activity and potential XSS activity.
- Built dashboards for security monitoring.
- Used IP reputation workflows with VirusTotal and AbuseIPDB.

### Network Security and Detection

- Captured and analyzed ICMP, TCP, HTTP, UDP, Netcat, and Nmap traffic using Wireshark.
- Analyzed TCP three-way handshakes and HTTP requests.
- Used Wireshark display and capture filters for network investigation.
- Performed host discovery and port scanning in controlled lab environments using Nmap.
- Configured Snort in sniffer, packet logging, IDS, and IPS modes.
- Created custom ICMP and SSH detection rules.
- Tested Snort alerts and IPS blocking using controlled traffic.

### Endpoint Security

- Installed and configured Wazuh agents on Linux and Windows systems.
- Practiced File Integrity Monitoring (FIM).
- Investigated file creation, modification, and deletion events.
- Monitored authentication failures.
- Observed unauthorized process/listener activity.
- Worked with Windows Event Viewer and Sysmon telemetry.

### Threat Hunting and Malware Analysis

- Practiced hypothesis-based threat hunting.
- Studied Indicators of Compromise (IOCs), Indicators of Attack (IOAs), and Indicators of Exposure (IOEs).
- Performed static and dynamic malware analysis in controlled lab environments.
- Generated and investigated file hashes using VirusTotal.
- Created custom YARA rules for suspicious strings and malware-related samples.
- Used network connections and process information during dynamic analysis.

### Incident Response

- Studied the incident response lifecycle and security playbooks.
- Investigated a simulated multi-stage security incident in QRadar involving authentication failures, successful SSH access, privilege escalation, and subsequent network activity.
- Correlated events across authentication and network activity.
- Documented findings and practiced escalation to higher-level investigation.
- Studied Jira-based security task management and SOAR workflows.

## Lab Environment

The practical exercises were performed in controlled lab environments using Linux and Windows virtual machines and intentionally generated security events.

Offensive security activities documented in this repository are presented strictly as controlled lab exercises for security monitoring, detection, and investigation purposes.

## Repository Structure

```
01-Linux-Kali/
02-Networking-Fundamentals/
03-Wireshark/
04-Nmap-Reconnaissance/
05-Metasploit-Lab/
06-Web-Security-Lab/
07-Linux-Firewall/
08-Snort-IDS-IPS/
09-Windows-Logs-Sysmon/
10-QRadar-SIEM/
11-Splunk-SIEM/
12-Threat-Intelligence/
13-Threat-Hunting/
14-Malware-Analysis-YARA/
15-Wazuh-Endpoint-Security/
16-Incident-Response-Jira-SOAR/
Purpose

This portfolio documents the practical cybersecurity skills developed during my CSA training and demonstrates
my hands-on exposure to SOC monitoring,security detection, log analysis, network analysis, endpoint monitoring,
threat hunting, malware analysis, and incident response.
