# Splunk Security Monitoring & Detection

## Overview

Hands-on Splunk SIEM exercises completed during EC-Council Certified SOC Analyst (CSA) training in a controlled virtual lab environment.

The exercises focused on log ingestion, SPL-based investigation, security monitoring, alert creation, dashboards, IP enrichment, and workflow actions.

---

## Objectives

- Understand Splunk SIEM and its data pipeline
- Ingest security logs into Splunk
- Search and analyze security events
- Practice SPL-based investigation
- Investigate authentication activity
- Analyze Apache web logs
- Detect directory brute-force activity
- Detect potential XSS activity
- Create alerts and dashboards
- Enrich IP addresses
- Use security reputation services in workflows

---

## Splunk Data Ingestion

Different methods of log ingestion were practiced during the training.

### Apache Access Logs

An Apache `access.log` file was uploaded into Splunk using an appropriate Apache sourcetype and index.

The ingested data was then searched and analyzed using SPL.

### TCP/UDP Data Input

Splunk was configured to monitor TCP/UDP port `3030`.

Netcat was used in the lab to generate data for the configured input.

### Splunk Forwarder

A Splunk Forwarder was configured on Kali Linux to send logs to Splunk.

Apache activity and other Linux security logs were then monitored through the forwarded data.

### Windows Logs

Windows system and firewall-related logs were also forwarded to Splunk for analysis.

---

## SPL Investigation

SPL was used to search, filter, organize, and summarize security events.

Examples of investigation activities included:

- Searching indexes
- Selecting specific fields
- Removing duplicate values
- Counting events by field
- Identifying common and rare values
- Filtering HTTP methods
- Filtering HTTP status codes
- Creating tables
- Renaming fields
- Creating statistics
- Visualizing security data

---

## Authentication Log Investigation

Linux authentication logs were analyzed to investigate suspicious login activity.

The investigation included:

- Failed authentication attempts
- Password-related events
- Invalid user activity
- Usernames involved in authentication attempts
- Source/attacker IP addresses

This provided practical exposure to identifying potential brute-force activity from authentication logs.

---

## Apache Web Log Investigation

Apache access logs were investigated using Splunk.

Fields examined included:

- Client IP
- HTTP method
- Requested file
- HTTP status
- User agent

HTTP response codes were used to distinguish successful and unsuccessful requests.

Examples included investigating:

```text
200 - Successful HTTP request
404 - Requested resource not found
Directory Brute-Force Detection

Controlled directory enumeration activity was generated against the lab Apache server.

Splunk was used to identify repeated unsuccessful HTTP requests.

A detection search focused on:

HTTP GET requests
HTTP 404 responses
Apache access logs
Client IP addresses

The activity was then used to create an alert for potential directory brute-force behavior.

The attacker IP was extracted and analyzed using SPL.

XSS Detection

A controlled XSS test was performed against the lab Apache environment.

The resulting web request was investigated through Apache access logs in Splunk.

A search was created to identify request patterns associated with the controlled XSS activity.

The investigation included:

Identifying the client IP
Filtering relevant Apache requests
Counting activity by client IP
Visualizing the results
Creating an alert for potential XSS activity
Malware-Related Event Monitoring

A request involving a file named:

malware.exe

was identified in Apache access logs during the lab.

A Splunk event type was created for the activity.

The event type included:

Event name
Priority
Visual identification

This demonstrated how Splunk knowledge objects can help categorize and highlight security-relevant events.

Nmap and Hydra Activity Searches

Splunk searches were also used to identify security-tool-related activity in collected logs.

Searches were performed for references to:

Nmap
Hydra

This demonstrated how security logs can be searched for activity associated with controlled security testing.

IP Enrichment

Public IP addresses extracted from logs were investigated for additional context.

Splunk's iplocation functionality was used to enrich IP-related data.

The enrichment helped provide additional geographic context for IP addresses during investigation.

Threat Intelligence Integration

IP reputation services were used to investigate suspicious public IP addresses.

The training included checking IP addresses using:

VirusTotal
AbuseIPDB

A public IP observed during the lab was found to have multiple security detections in VirusTotal.

This demonstrated how threat intelligence can support SIEM investigations.

Workflow Actions

Splunk workflow actions were created to simplify IP reputation checks.

Workflow actions were configured for:

VirusTotal
AbuseIPDB

The client IP field was used dynamically so an analyst could use the observed IP address when performing reputation checks.

This demonstrated how external threat intelligence can be incorporated into the analyst workflow.

Dashboards

Splunk dashboards were created to provide a centralized view of security activity.

Dashboard panels included:

Real-time Apache logs
XSS-related IP activity
Authentication failures
Directory brute-force activity
Attacker IP information

Visualization was also used to represent security activity, including IP-based activity.

Splunk Knowledge Objects

The training introduced Splunk knowledge objects used to organize and interpret security data.

The exercises included:

Event types
Fields
Tags

Event types were created for security-relevant activity such as:

Malware-related requests
Brute-force activity

Tags were also used in SPL searches.

Security Monitoring Workflow

The practical exercises demonstrated a basic SIEM monitoring workflow:

Log Collection
      ↓
Data Ingestion
      ↓
Search & Filtering
      ↓
Event Analysis
      ↓
Detection
      ↓
Alert Creation
      ↓
Investigation
      ↓
Threat Intelligence Enrichment
      ↓
Dashboard / Reporting
Key Skills Practiced
Splunk SIEM
SPL
Log ingestion
Splunk Forwarder
Apache log analysis
Linux authentication log analysis
Windows log monitoring
Security event investigation
Brute-force detection
Directory enumeration detection
XSS detection
Alert creation
Dashboard creation
Event types
Fields and tags
IP enrichment
VirusTotal
AbuseIPDB
Workflow actions
SOC Analyst Perspective

The exercises demonstrated how a SOC analyst can use Splunk to move from raw security telemetry to actionable investigation.

The workflow included:

Collecting logs from multiple sources
Searching for suspicious activity
Filtering relevant events
Identifying source IP addresses
Creating detections and alerts
Visualizing security activity
Enriching indicators with threat intelligence
Supporting investigation through automated workflow actions

Learning Outcome

Developed hands-on familiarity with Splunk SIEM, SPL-based security investigation, multi-source log ingestion, detection and alert creation, dashboard development, IP enrichment, and threat-intelligence-assisted investigation.

Note: The security testing activities documented here were performed in controlled cybersecurity training/lab environments as part of CSA training.
