# QRadar Multi-Stage Incident Investigation

## Overview

A simulated multi-stage security incident was investigated using IBM QRadar during EC-Council Certified SOC Analyst (CSA) training.

The investigation focused on correlating authentication and network activity to understand how a sequence of suspicious events developed into a broader security incident.

The exercise was performed in a controlled virtual lab environment.

---

## Investigation Objective

The objective was to investigate suspicious authentication activity and determine whether the events represented a larger security incident.

The investigation involved:

- Authentication failures
- Invalid user activity
- Successful SSH authentication
- Privilege escalation
- Root-level activity
- Network activity
- Possible file transfer activity
- Correlation of activity from different source IP addresses
- Incident documentation and escalation

---

## SIEM Environment

**SIEM:** IBM QRadar Community Edition

### QRadar Features Used

- Log Activity
- Network Activity
- Offense investigation
- AQL searches
- Event filtering
- Flow analysis
- Detection rules
- Dashboard investigation
- Offense management
- False-positive tuning
- Incident documentation

---

## Initial Detection

The investigation began with an offense involving suspicious authentication activity.

The offense contained multiple authentication-related events, including:

- Failed password attempts
- Invalid usernames
- Unsuccessful authentication
- A subsequent successful login

The activity was associated with a source IP attempting access to a Linux server.

---

## Investigation Timeline

The investigation revealed the following sequence:

```text
Multiple Failed Login Attempts
              ↓
Invalid User Activity
              ↓
Successful SSH Login
              ↓
Privilege Escalation
              ↓
Root-Level Activity
              ↓
Python HTTP Server Started
              ↓
Port 8000 Network Activity
              ↓
confidential.txt Activity
              ↓
Different Source IP Observed

This sequence indicated that the authentication events needed to be investigated together rather than treated as isolated alerts.

Authentication Investigation

QRadar Log Activity was used to examine authentication events associated with the suspicious source IP.

The investigation identified:

Multiple failed login attempts
Attempts involving different usernames
Invalid user activity
A successful SSH authentication
The source IP associated with the activity
The destination Linux server

The successful authentication was particularly important because it followed repeated authentication failures from the same source.

Successful SSH Authentication

A successful SSH authentication event was identified after the failed login activity.

The event indicated that the kali account successfully authenticated through SSH from the suspicious source IP.

The successful login was correlated with the earlier authentication failures to determine whether the activity represented a possible password-cracking or brute-force sequence.

Privilege Escalation Investigation

After the successful login, another event showed execution of:

sudo su

This activity indicated a transition to elevated privileges.

The source and destination information was correlated with the earlier authentication activity.

The sequence therefore progressed from unsuccessful authentication attempts to successful access followed by privilege escalation.

Root-Level Activity

Following privilege escalation, root-level activity was observed.

The investigation then examined subsequent activity to determine what actions occurred after elevated access was obtained.

This helped establish a broader timeline rather than stopping the investigation at the successful login.

Python HTTP Server Activity

After the privilege escalation activity, the investigation identified a Python HTTP server being started using:

/usr/bin/python3 -m http.server

The associated network activity was observed on:

Port 8000

This activity was investigated through QRadar Network Activity.

Network Activity Investigation

QRadar Network Activity was used to examine traffic associated with port 8000.

The investigation identified:

A source IP
A destination system
HTTP activity
HTTP response code 200
Activity involving confidential.txt
A different source IP associated with subsequent network activity

The network events were correlated with the earlier authentication and privilege-escalation events.

Correlation of Events

The investigation demonstrated the importance of correlating multiple types of telemetry.

The overall sequence was:

Stage	Observed Activity
1	Multiple authentication failures
2	Invalid user activity
3	Successful SSH authentication
4	Privilege escalation using sudo su
5	Root-level activity
6	Python HTTP server started
7	Network activity on port 8000
8	confidential.txt activity
9	Different source IP observed

Instead of investigating each event independently, the events were correlated into a single incident timeline.

Offense Analysis

The QRadar offense provided additional context about the incident.

The investigation examined:

Offense magnitude
Severity
Relevance
Credibility
Source IP
Destination IP
Event count
Event categories
Usernames
Recent events
Network activity

The offense contained a large number of authentication-related events and was associated with password-cracking/brute-force activity.

Detection Engineering

During the QRadar training, detection rules were also created and tested.

One detection rule was configured to identify repeated login failures using event properties and a threshold of multiple events within a short time period.

The rule was tested by generating controlled failed-login activity and observing the resulting offense.

Other detection exercises included:

Flow-based detection
Insecure HTTP activity
Data-exfiltration-related activity
Event and flow correlation
False-Positive Tuning

False-positive tuning was practiced during the QRadar exercises.

A scenario involving an administrator entering an incorrect password was used to understand how legitimate activity can generate security alerts.

The exercise involved using event information such as:

Event/QID information
Source IP
Destination/server information
User context

The objective was to improve detection quality while reducing unnecessary alerts.

Investigation Conclusion

The simulated investigation indicated a multi-stage security incident in which:

Repeated authentication failures occurred.
A successful SSH login followed the failed attempts.
Privilege escalation occurred after successful access.
Root-level activity was observed.
A Python HTTP server was started.
Network activity occurred over port 8000.
Activity involving confidential.txt was observed.
A different source IP was associated with subsequent network activity.

The activity was treated as suspicious and documented for further investigation.

Incident Documentation & Escalation

The investigation findings were documented as part of the training exercise.

The scenario was identified as requiring further investigation at a higher level, and the importance of L2/L3 escalation was discussed.

The exercise demonstrated how a SOC analyst can:

Identify suspicious activity
Correlate events
Build an incident timeline
Investigate authentication activity
Investigate network activity
Identify privilege escalation
Document findings
Escalate an incident for further investigation
Skills Demonstrated
SIEM investigation
QRadar Log Activity analysis
QRadar Network Activity analysis
QRadar offense investigation
AQL-based investigation
Authentication log analysis
Brute-force detection
SSH activity analysis
Privilege escalation identification
Network activity correlation
Incident timeline development
Detection rule creation
False-positive tuning
Incident documentation
Security escalation

Key Takeaway

This exercise demonstrated the importance of correlating authentication, endpoint, and network telemetry during security investigations.
A single failed-login event may not provide enough context. Correlating repeated authentication failures, successful access, privilege escalation, and subsequent network activity can reveal the progression of a larger security incident.

Note: This investigation was performed in a controlled cybersecurity training/lab environment as part of CSA training.
