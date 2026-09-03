# CSA Hands-On Cybersecurity Lab Portfolio

## SOC Analyst | Cybersecurity Operations | SIEM | Threat Detection

Hands-on cybersecurity lab portfolio developed during EC-Council Certified SOC Analyst (CSA) training.

This repository documents practical exercises in security monitoring, SIEM operations, log analysis, network traffic analysis, threat detection, endpoint monitoring, threat hunting, malware analysis, and incident response.

All security testing and offensive activities documented here were performed in controlled training/lab environments.

---

## 🛡️ Core SOC Skills

- SIEM monitoring and investigation
- Security log analysis
- Authentication and access monitoring
- Network traffic analysis
- Threat detection and alert investigation
- Detection rule creation and validation
- False-positive tuning
- Endpoint monitoring and File Integrity Monitoring
- Threat hunting
- Threat intelligence and IOC analysis
- Malware analysis
- Incident response
- Security dashboards and reporting
- Security workflow automation concepts

---

## 🔧 Security Tools

### SIEM & Security Monitoring
- IBM QRadar
- Splunk
- Wazuh

### Network Security & Analysis
- Wireshark
- Snort IDS/IPS
- Nmap
- iptables
- Netcat

### Endpoint & Operating Systems
- Windows Event Viewer
- Sysmon
- Kali Linux
- Linux

### Threat Intelligence & Malware Analysis
- VirusTotal
- AbuseIPDB
- YARA

### Security Testing Tools Used in Controlled Labs
- Metasploit
- Hydra
- Medusa
- SQLMap
- DIRB
- hping3

### Security Operations
- Jira
- SOAR concepts

---

# ⭐ Key Practical Investigations

## 1. QRadar Multi-Stage Incident Investigation

Investigated a simulated multi-stage security incident by correlating authentication and network activity.

### Investigation sequence

```text
Multiple Failed Logins
        ↓
Invalid User Activity
        ↓
Successful SSH Login
        ↓
Privilege Escalation
        ↓
Root-Level Activity
        ↓
Python HTTP Server
        ↓
Port 8000 Network Activity
        ↓
confidential.txt Activity
        ↓
Different Source IP
        ↓
Incident Documentation & Escalation
Work performed
Investigated authentication failures and successful SSH authentication.
Correlated source and destination IP addresses.
Identified privilege escalation activity.
Investigated root-level activity.
Analyzed subsequent network activity on port 8000.
Correlated activity involving confidential.txt.
Observed activity involving a different source IP.
Built an incident timeline.
Documented findings.
Identified the need for further L2/L3 investigation.

Primary tools: IBM QRadar, AQL, Linux authentication logs, Network Activity.

2. Splunk Security Monitoring & Detection

Performed hands-on SIEM exercises using Splunk with Linux, Apache, SSH, Windows, and firewall logs.

Work performed
Ingested Apache access logs.
Monitored logs through TCP/UDP input.
Configured Splunk Forwarder log collection.
Forwarded Kali and Windows security logs.
Analyzed authentication failures.
Investigated Apache access activity.
Used SPL for filtering, deduplication, statistics, and visualization.
Investigated directory brute-force activity.
Created an alert for suspicious 404/GET activity.
Created an alert for potential XSS activity.
Built security monitoring dashboards.
Created event types and knowledge objects.
Used IP enrichment with iplocation.
Created VirusTotal and AbuseIPDB workflow actions for IP reputation checks.

Primary tools: Splunk, SPL, Apache logs, SSH/authentication logs, Windows logs.

3. Wazuh Endpoint Monitoring & FIM

Performed endpoint monitoring exercises using Wazuh agents on Linux and Windows systems.

Work performed
Deployed Wazuh agents.
Monitored endpoint activity.
Configured and tested File Integrity Monitoring.
Detected file creation.
Detected file modification.
Detected file deletion.
Investigated authentication failures.
Observed unauthorized process/listener activity.
Connected endpoint monitoring with incident response concepts.

Primary tools: Wazuh, Linux, Windows.

4. Snort IDS/IPS Detection

Configured and tested Snort as a network intrusion detection and prevention system.

Work performed
Used Snort in sniffer mode.
Used packet logging mode.
Configured Snort IDS.
Created custom ICMP detection rules.
Created custom SSH detection rules.
Generated controlled traffic to validate alerts.
Investigated Nmap-generated alerts.
Tested Snort IPS functionality.
Observed blocking behavior during controlled SSH testing.

Primary tools: Snort, Wireshark, Nmap.

5. Threat Hunting & Malware Analysis

Practiced threat hunting and malware analysis concepts using controlled lab samples and security intelligence sources.

Threat Hunting
Studied hypothesis-based threat hunting.
Worked with Indicators of Compromise (IOCs).
Studied Indicators of Attack (IOAs).
Studied Indicators of Exposure (IOEs).
Reviewed threat intelligence as part of the hunting process.
Studied MITRE ATT&CK concepts.
Malware Analysis
Studied static, dynamic, and hybrid malware analysis.
Generated file hashes and investigated them using VirusTotal.
Investigated suspicious malware samples in controlled environments.
Created custom YARA rules.
Used strings and conditions in YARA rules.
Created rules for suspicious and malware-related samples.
Used process and network information during dynamic analysis.
Used netstat to observe established connections and associated process information.

Primary tools: YARA, VirusTotal, Kali Linux, Windows, MITRE ATT&CK.

📚 Training Areas
Linux & Networking
Linux/Kali administration
Linux filesystem and permissions
Linux processes and services
TCP/IP fundamentals
IPv4 and IPv6
TCP and UDP
Network ports
NAT
HTTP fundamentals
Network Analysis
Wireshark packet capture
ICMP analysis
TCP three-way handshake analysis
HTTP request analysis
Netcat traffic analysis
Nmap traffic analysis
PCAP investigation
Display and capture filters
Network Security
Host discovery
Port scanning
Service/version detection
Nmap NSE scripts
Snort IDS/IPS
Linux firewall configuration
Windows firewall logging
Windows Security
Windows Event Viewer
Security event analysis
Authentication monitoring
Account activity monitoring
Sysmon telemetry
Process and network monitoring
SIEM
IBM QRadar
QRadar Log Activity
QRadar Network Activity
QRadar offenses
QRadar AQL
Detection rules
False-positive tuning
Dashboards
Reports
Splunk data ingestion
Splunk SPL
Splunk alerts
Splunk dashboards
Knowledge objects
Endpoint Security
Wazuh
Endpoint monitoring
File Integrity Monitoring
Authentication monitoring
Process/listener monitoring
Threat Intelligence & Hunting
Threat intelligence lifecycle
Threat actors
APT concepts
IOC / IOA / IOE
Threat hunting methodology
MITRE ATT&CK
Malware Analysis
Static analysis
Dynamic analysis
Hybrid analysis
File hashing
VirusTotal
YARA
Process analysis
Network connection analysis
Incident Response
Incident response lifecycle
Preparation
Detection & analysis
Containment
Eradication
Recovery
Post-incident activity
Incident response playbooks
Incident documentation
Jira
SOAR concepts and playbooks
📁 Repository Structure

01-Linux-Kali/
02-Networking-Fundamentals/
03-Wireshark/
04-Nmap-Reconnaissance/
05-Metasploit-Lab/
06-Apache-DoS-Malware-Lab/
07-SSH-RDP-Phishing-Web-Security/
08-Linux-Firewall-Logging/
09-Snort-IDS-IPS/
10-Windows-Event-Logs-Sysmon/
11-QRadar-SIEM/
12-Splunk-SIEM/
13-Threat-Intelligence-Threat-Hunting-Lab/
14-Malware-Analysis-YARA/
15-Wazuh-EDR-FIM/
16-Incident-Response-Jira-SOAR/

🎯 Purpose

This portfolio documents the practical cybersecurity skills developed during EC-Council Certified SOC Analyst (CSA) training.

The focus of the portfolio is defensive security operations, including:

Security monitoring
SIEM operations
Log analysis
Threat detection
Incident investigation
Network security monitoring
Endpoint monitoring
Threat hunting
Threat intelligence
Malware analysis
Incident response

Offensive security activities included in the repository were performed strictly as controlled cybersecurity training exercises and are documented from a defensive SOC perspective.
