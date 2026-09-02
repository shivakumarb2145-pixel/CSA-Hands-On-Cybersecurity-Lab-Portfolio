# IBM QRadar SIEM — SOC Monitoring & Investigation Lab

## Overview

Hands-on IBM QRadar SIEM exercises completed during EC-Council Certified SOC Analyst (CSA) training in a controlled virtual lab environment.

The sessions covered SIEM architecture, log ingestion, event and flow analysis, AQL searches, offense investigation, detection-rule creation, false-positive tuning, dashboards, assets, and security reporting.

## Objectives

- Understand SIEM architecture and SOC operations
- Work with IBM QRadar Community Edition
- Understand QRadar components
- Configure Linux log forwarding
- Ingest authentication logs into QRadar
- Investigate security events
- Perform AQL-based searches
- Analyze network flows
- Investigate QRadar offenses
- Create detection rules
- Practice false-positive tuning
- Manage assets
- Create dashboards and reports
- Document and escalate security incidents

## Lab Environment

The exercises were performed in a controlled virtual lab using QRadar Community Edition and Kali Linux.

Linux security logs were forwarded to QRadar using rsyslog.

---

## QRadar Components Studied

Studied the major QRadar components and their roles, including:

- Log Sources
- Event Collector
- Event Processor
- Data Node
- Console
- Users
- Network / Flow Sources
- Flow Collector
- Flow Processor
- Vulnerability Scanner

Also studied QRadar deployment models:

- All-in-one
- Distributed

---

## QRadar Interface

Worked with the main QRadar areas:

- Dashboard
- Offenses
- Log Activity
- Network Activity
- Assets
- Reports
- Admin

These areas were used during monitoring, investigation, and reporting exercises.

---

## Log Ingestion

Practiced log ingestion using the **push model**.

Configured rsyslog on Kali Linux to forward logs to the QRadar system.

The configuration used the Linux rsyslog service to send security-related logs to the QRadar IP address and port.

A controlled SSH authentication-testing exercise was then performed against the Kali system to generate authentication events.

The resulting logs were observed in QRadar.

### Log Investigation Flow

```text
Kali Linux
    ↓
rsyslog
    ↓
QRadar
    ↓
Log Activity
    ↓
Event Analysis
    ↓
Offense Investigation
```

---

## Log Activity

Used QRadar Log Activity to investigate incoming events.

Practiced filtering and searching using:

- Event Name
- Log Source
- Source IP
- Destination IP
- QID
- Multiple search criteria
- Time ranges

Also practiced saving search criteria for repeated investigations.

Investigated event counts, unique IP addresses, usernames, and event names.

---

## AQL Practice

Practiced QRadar Ariel Query Language (AQL) for event investigation.

Examples used during training included:

```sql
SELECT * FROM events
```

```sql
SELECT sourceip FROM events
```

```sql
SELECT sourceip, destinationip, sourceport, destinationport FROM events
```

```sql
SELECT username FROM events
```

```sql
SELECT * FROM events WHERE sourceip='SOURCE_IP'
```

```sql
SELECT * FROM events WHERE destinationip='DESTINATION_IP'
```

```sql
SELECT * FROM events WHERE destinationport='22'
```

```sql
SELECT sourceip AS "AttackerIP",
destinationip AS "TargetIP"
FROM events
```

```sql
SELECT sourceport,
sourceip AS "AttackerIP",
destinationip AS "TargetIP"
FROM events
WHERE sourceport='22'
```

```sql
SELECT sourceip AS "AttackerIP",
destinationip AS "TargetIP"
FROM events
GROUP BY sourceip
```

Also practiced time-based searches such as:

```sql
SELECT * FROM events LAST 1 HOURS
```

```sql
SELECT * FROM events LAST 7 MINUTES
```

```sql
SELECT * FROM events LAST 30 DAYS
```

---

## QRadar Functions Practiced

Used QRadar functions to identify event and log-source information.

Examples included:

```sql
SELECT QIDNAME(qid) FROM events
```

```sql
SELECT qid, QIDNAME(qid) FROM events
```

```sql
SELECT LOGSOURCENAME(logsourceid), logsourceid FROM events
```

Also practiced filtering using:

- `WHERE`
- `AND`
- `OR`
- `LIKE`
- `IS NOT NULL`
- `GROUP BY`
- `ORDER BY`
- `LIMIT`

---

## Network Activity

Worked with QRadar Network Activity to investigate network flows.

Practiced examining:

- Protocol
- First packet time
- Last packet time
- Storage time
- Source IP
- Destination IP
- Source port
- Destination port

Generated network activity using controlled lab traffic such as ICMP and HTTP communication.

### ICMP Investigation

Generated ping traffic and filtered network activity using the ICMP protocol.

### HTTP Investigation

Generated HTTP traffic by visiting HTTP websites and examined:

- Source IP
- Destination IP
- Source port
- Destination port
- HTTP response code
- Server information
- TCP flags

Also studied HTTPS traffic.

---

## Flow Analysis

Studied QRadar flow types, including:

- Standard Flow
- Superflow

Also reviewed the different Superflow types covered during training.

AQL concepts practiced for events were also applied to flow-based investigation.

---

## QRadar Dashboards

Created and worked with QRadar dashboard panels.

Panels included:

- Top Applications
- Most Recent Offenses
- My Offenses
- Top Sources
- Top Local Destinations

The dashboard was used to provide a centralized view of security activity.

---

## Asset Management

Studied QRadar asset information and asset discovery.

Reviewed asset information including:

- Asset ID
- IP address
- MAC address
- DNS
- NetBIOS
- Asset name
- Location
- Description
- Operating system
- CVSS
- Weight and compliance
- Owners

Also studied server discovery and vulnerability-assessment-related asset information.

---

# Offense Investigation

## Offense Management

Worked with QRadar offenses and reviewed:

- Offense ID
- Description
- Offense type
- Magnitude
- Source IP
- Destination IP
- Category
- Severity
- Relevance
- Credibility

Practiced assigning offenses to users and viewing assigned offenses through the dashboard.

---

## Multi-Stage Security Incident Investigation

One of the main QRadar exercises involved investigating a simulated multi-stage security incident.

The offense represented a sequence of activity involving:

```text
Multiple failed login attempts
        ↓
Invalid user activity
        ↓
Successful SSH authentication
        ↓
Privilege escalation
        ↓
Root access
        ↓
Python HTTP server started
        ↓
Port 8000 network activity
        ↓
confidential.txt activity
        ↓
Different source IP observed
```

The investigation involved correlating authentication and network activity from the same security environment.

---

## Authentication Investigation

Reviewed Log Activity associated with the source IP involved in the offense.

Observed authentication events including:

- Password failures
- Invalid users
- Unsuccessful authentication
- Successful SSH authentication

A successful authentication event showed an SSH session associated with the Kali account.

The authentication timeline was used to understand the sequence of activity leading to the successful login.

---

## Privilege Escalation Investigation

Investigated subsequent activity associated with privilege escalation.

The investigation identified the execution of:

```text
sudo su
```

The activity indicated a transition to elevated privileges within the lab system.

The event was correlated with the same source and destination information observed during the earlier authentication activity.

---

## Python HTTP Server Investigation

Following privilege escalation, the investigation identified a Python HTTP server process:

```text
/usr/bin/python3 -m http.server
```

Network activity associated with port:

```text
8000
```

was then investigated in QRadar Network Activity.

---

## File Transfer Investigation

The network investigation identified activity involving:

```text
confidential.txt
```

A different source IP was observed during the network activity.

The events were correlated to understand the progression from authentication to privilege escalation and subsequent file-transfer-related network activity.

---

## Incident Timeline

The investigation was documented as a timeline:

```text
1. Multiple authentication failures
2. Invalid user activity
3. Successful SSH login
4. Privilege escalation using sudo su
5. Root-level activity
6. Python HTTP server started
7. Port 8000 network activity observed
8. confidential.txt activity identified
9. Different source IP observed
10. Incident documented and escalated for further investigation
```

---

## Detection Rule Creation

Created QRadar event detection rules during the training.

One detection exercise used:

- QID
- Event properties
- Source IP
- Log source
- Event count
- Time window
- Severity
- Credibility
- Relevance

A rule was configured to identify repeated failed-login activity, including a threshold of multiple events within a short time period.

Controlled failed-login activity was generated to validate the detection.

---

## Flow-Based Detection

Created a QRadar flow rule focused on traffic involving destination port 80.

The rule was tested by generating HTTP traffic in the lab.

This demonstrated how network-flow characteristics can be used as detection criteria.

---

## Data Exfiltration Detection

Created and tested a detection rule related to data-exfiltration activity during the training exercises.

The rule was used to understand how suspicious network behavior can be identified through QRadar flow information.

---

## False-Positive Tuning

Practiced tuning detections to reduce false positives.

One exercise focused on distinguishing expected administrator authentication failures from potentially suspicious activity.

The tuning process considered factors such as:

- Event type
- QID
- Administrator IP
- Server IP
- Expected administrative behavior

This demonstrated the importance of balancing detection sensitivity with false-positive reduction.

---

## Reports

Created QRadar reports covering security activity such as:

- Top source IP addresses
- Top offenses

Reports were used to summarize security information for monitoring and analysis.

---

## SOC Investigation Workflow

The QRadar exercises followed a practical investigation workflow:

```text
Log Collection
      ↓
Event / Flow Analysis
      ↓
Detection
      ↓
Offense Creation
      ↓
Alert Investigation
      ↓
Timeline Correlation
      ↓
Incident Documentation
      ↓
Escalation
```

---

## Key Skills Practiced

- IBM QRadar Community Edition
- SIEM operations
- Log ingestion
- rsyslog
- Log Activity
- Network Activity
- AQL
- Event analysis
- Flow analysis
- Offense investigation
- Detection-rule creation
- False-positive tuning
- Dashboard creation
- Asset management
- Security reporting
- Incident documentation
- SOC investigation workflow

## Learning Outcome

Developed practical experience using IBM QRadar for security monitoring, log analysis, detection engineering, offense investigation, and incident documentation.

The multi-stage incident investigation provided hands-on experience correlating authentication events, privilege escalation, process activity, network flows, and file-transfer-related activity into a single security timeline.

> **Note:** All security events, authentication testing, detection validation, and incident scenarios documented in this section were performed within controlled cybersecurity training environments.
