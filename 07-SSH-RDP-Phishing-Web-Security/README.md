# SSH, RDP, Phishing & Web Security Lab

## Overview

Hands-on cybersecurity exercises completed during CSA training in controlled lab environments. The sessions covered SSH and RDP authentication testing, password-attack detection, phishing awareness, web application security, database security, directory enumeration, and cross-site scripting.

## Objectives

- Configure and access SSH services
- Understand SSH authentication activity
- Perform controlled authentication testing
- Analyze authentication failures and successful logins
- Understand RDP authentication and remote access
- Study phishing and social-engineering techniques
- Identify common phishing indicators
- Understand SQL injection concepts in vulnerable lab applications
- Explore MySQL services in a controlled environment
- Perform directory enumeration against lab web servers
- Understand cross-site scripting (XSS)
- Observe web security activity through server logs

## Lab Environment

The exercises were performed in controlled virtual lab environments using Kali Linux, Windows test systems, Metasploitable, and intentionally vulnerable web applications.

All authentication testing and web-security exercises were performed as part of the CSA training environment.

---

## SSH Security Lab

Configured and worked with SSH services between the lab systems.

The sessions included:

- Starting and managing the SSH service
- Establishing SSH connections
- Understanding SSH authentication
- Observing successful and failed authentication attempts
- Identifying the source of authentication attempts
- Reviewing authentication activity from a defensive perspective

Authentication activity was later connected with Linux authentication logs and SIEM investigations.

---

## Controlled SSH Authentication Testing

Practiced dictionary-based authentication testing against a controlled SSH lab target.

The exercises used:

- Hydra
- Medusa
- Custom username lists
- Custom password lists

The objective was to understand how repeated authentication failures appear in security logs and how valid credentials can be identified within a controlled training environment.

### Defensive Investigation

The activity demonstrated the importance of monitoring:

- Repeated authentication failures
- Invalid usernames
- Source IP addresses
- Target accounts
- Successful authentication following multiple failures
- Authentication timestamps

These concepts were later used during QRadar and Splunk investigations.

---

## RDP Security Lab

Studied Windows Remote Desktop Protocol (RDP) authentication in the controlled Windows lab.

The exercise included controlled authentication testing and remote access using an RDP client.

The session helped demonstrate:

- RDP authentication
- Remote Windows access
- Authentication failures
- Successful authentication
- The importance of monitoring remote-access activity

---

## Phishing & Social Engineering Lab

Studied phishing and social-engineering techniques in a controlled training environment.

A phishing simulation was performed using a locally controlled training setup to understand how deceptive login pages can be used to capture submitted credentials.

The exercises included simulated login pages for commonly used online services.

### Phishing Awareness

The session also focused on identifying phishing indicators, including:

- Suspicious links
- Unexpected login requests
- Fake authentication pages
- Untrusted domains
- Requests for credentials
- Social-engineering techniques

The primary objective was to understand how phishing activity can be detected and investigated from a security-awareness and SOC perspective.

---

## SQL Injection Lab

Studied SQL injection using intentionally vulnerable web applications in the training environment.

The exercises demonstrated how improperly handled user input can affect database queries.

Topics practiced included:

- SQL injection concepts
- Query manipulation
- Authentication bypass concepts
- Vulnerable application behavior
- Database interaction
- Administrative access concepts in vulnerable applications

The exercises were performed against intentionally vulnerable training targets.

---

## MySQL Security Lab

Worked with MySQL services in the controlled Metasploitable environment.

The exercises included:

- Identifying the MySQL service
- Understanding the MySQL service port
- Controlled authentication testing
- Connecting to the MySQL service
- Exploring databases and tables
- Examining user-related database information

The exercise demonstrated the importance of protecting database services and monitoring unauthorized authentication attempts.

---

## Directory Enumeration Lab

Performed directory and file enumeration against a controlled Apache web server using DIRB.

The exercise identified accessible and hidden web directories and files.

The activity also demonstrated how directory-enumeration requests appear in Apache access logs.

### Log Analysis

Observed HTTP requests including:

- Successful requests
- Not-found responses
- Repeated directory requests
- Source IP addresses
- Requested paths

This activity was later connected with Splunk-based web log investigation and alert creation.

---

## Cross-Site Scripting (XSS) Lab

Studied cross-site scripting using a controlled vulnerable web application.

The exercise demonstrated how malicious script input can be submitted through vulnerable web functionality.

The activity was also observed through Apache access logs.

### Defensive Perspective

The exercise helped identify useful indicators for web-security monitoring, including:

- Suspicious request parameters
- Encoded script-related characters
- Unusual HTTP requests
- Repeated requests from the same source
- Abnormal web application input

These indicators were later used during Splunk searches and alert creation.

---

## Security Monitoring Connection

The authentication and web-security exercises generated activity that could be investigated using security logs.

Examples included:

```text
Authentication failures
        ↓
Source IP identification
        ↓
Successful authentication
        ↓
Web requests
        ↓
HTTP response codes
        ↓
Log analysis
        ↓
Detection and investigation
```

The exercises helped connect security testing activity with the logs and telemetry that a SOC analyst would investigate.

---

## Tools Used

- Kali Linux
- SSH
- Hydra
- Medusa
- RDP
- rdesktop
- DIRB
- Apache
- MySQL
- Wireshark
- Splunk
- QRadar

## Key Skills Practiced

- SSH security monitoring
- Authentication log analysis
- RDP security concepts
- Password-attack detection
- Phishing awareness
- Social-engineering awareness
- Web application security
- SQL injection concepts
- MySQL security
- Directory enumeration
- XSS detection concepts
- Apache log analysis
- SIEM investigation

## Learning Outcome

Developed practical understanding of authentication security, remote-access activity, phishing awareness, and common web-security issues through controlled cybersecurity lab exercises.

The sessions also demonstrated how authentication and web activity can generate useful security telemetry for SOC monitoring, detection, investigation, and incident response.

> **Note:** All authentication testing, phishing simulations, database testing, directory enumeration, and web-security exercises documented here were performed against controlled training systems and intentionally vulnerable lab environments.
