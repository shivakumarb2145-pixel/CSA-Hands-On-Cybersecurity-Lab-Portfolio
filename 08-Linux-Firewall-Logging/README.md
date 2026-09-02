# Linux Firewall & Security Logging Lab

## Overview

Hands-on firewall and security logging exercises completed during CSA training in controlled lab environments. The sessions focused on Linux logs, iptables firewall configuration, traffic filtering, firewall logging, SSH protection, and Windows Firewall logging.

## Objectives

- Understand Linux security logs
- Explore common files under `/var/log`
- Analyze Apache and authentication logs
- Understand iptables firewall chains
- Create and remove firewall rules
- Block and reject network traffic
- Restrict SSH access
- Configure firewall logging
- Investigate firewall events through system logs
- Understand Windows Defender Firewall logging

## Lab Environment

The exercises were performed using Kali Linux, Ubuntu, and Windows lab systems in a controlled training environment.

---

## Linux Security Logs

Explored the Linux `/var/log` directory and examined different system and application logs.

Logs reviewed during the sessions included:

- `boot.log`
- `apt`
- `dpkg.log`
- `wtmp`
- `btmp`
- `utmp`
- Apache logs
- `auth.log`
- `syslog`

These logs were used to understand how system activity, authentication activity, and web-server activity can be recorded for security investigation.

---

## Apache Access Log Analysis

Reviewed Apache access logs to identify web activity generated during controlled security-testing exercises.

The logs were analyzed for:

- Source IP addresses
- Request timestamps
- Requested resources
- HTTP status codes
- HTTP requests
- Directory-enumeration activity
- XSS-related requests

Directory enumeration and XSS exercises performed earlier in the CSA training were visible in the Apache `access.log`.

This demonstrated how web attacks can leave useful evidence in server logs.

---

## Linux Authentication Logs

Reviewed Linux authentication activity through:

```text
/var/log/auth.log
```

The sessions included observing authentication failures and identifying the source IP associated with repeated SSH authentication attempts.

The logs helped identify:

- Failed authentication attempts
- Invalid users
- Source IP addresses
- Successful authentication
- SSH activity
- Authentication timestamps

These observations were later used during SIEM investigations in QRadar and Splunk.

---

## iptables Firewall

Studied Linux firewall concepts using `iptables`.

The sessions covered the main iptables chains:

```text
INPUT
OUTPUT
FORWARD
```

The exercises demonstrated how firewall rules can control incoming and outgoing network traffic.

---

## ICMP Filtering

Configured an input firewall rule to block ICMP echo requests.

The rule was later removed and a reject-based configuration was tested to understand the difference between dropping and rejecting traffic.

The behavior was verified by generating ICMP traffic from the lab systems.

### Defensive Concept

This exercise demonstrated how firewall rules can be used to control unwanted network traffic and reduce exposure to certain types of network activity.

---

## Outbound Traffic Filtering

Configured output firewall rules to control outbound traffic from the Linux system.

The sessions included testing rules that blocked:

- Traffic to a specific website IP address
- HTTP traffic over TCP port 80

The behavior was validated by attempting to access websites after applying the firewall rules.

---

## SSH Protection

Configured SSH on the Kali Linux lab system and performed controlled authentication testing from another lab machine.

The authentication logs were then reviewed to identify the source IP of the authentication attempts.

A firewall rule was configured to:

- Block SSH traffic on TCP port 22
- Allow SSH access only from the designated administrative lab IP

This demonstrated how host-based firewall rules can be used to restrict remote administration access.

---

## Firewall Logging

Configured iptables rules to generate firewall log entries.

Custom log prefixes were used for identifying firewall activity, including:

```text
FIREWALL:
FIREWALL OUT
```

The resulting entries were observed in the system logging infrastructure.

The logs were then filtered to investigate:

- ICMP traffic
- Source addresses
- Destination addresses
- TCP ports
- Firewall actions

This demonstrated how firewall events can become useful security telemetry for a SOC analyst.

---

## Investigating Authentication Activity

During the controlled SSH authentication exercise, repeated authentication attempts generated entries in the authentication logs.

The attacker/test-system IP was identified from the logs.

This provided practical experience with the basic investigation process:

```text
Authentication Event
        ↓
Identify Source IP
        ↓
Review Timestamp
        ↓
Check Target Account
        ↓
Determine Success/Failure
        ↓
Apply Defensive Control
```

---

## Windows Firewall Logging

The sessions also covered Windows Defender Firewall.

The exercises included:

- Reviewing inbound firewall rules
- Reviewing outbound firewall rules
- Configuring firewall behavior
- Enabling firewall logging
- Generating ICMP traffic
- Reviewing firewall-related log entries

This provided experience with host-based firewall monitoring across both Linux and Windows environments.

---

## SOC Investigation Perspective

Firewall and system logs provide important telemetry for security monitoring.

Useful investigation fields include:

- Timestamp
- Source IP
- Destination IP
- Source port
- Destination port
- Protocol
- Action
- Authentication result
- Username
- Requested resource

These fields can help a SOC analyst determine whether activity represents normal behavior, a false positive, or potentially suspicious activity.

---

## Key Skills Practiced

- Linux security logging
- `/var/log` investigation
- Apache log analysis
- Authentication log analysis
- iptables
- INPUT / OUTPUT / FORWARD chains
- ICMP filtering
- HTTP traffic filtering
- SSH access control
- Firewall logging
- Windows Defender Firewall
- Security event investigation
- Source IP identification
- Network traffic filtering

## Learning Outcome

Developed practical understanding of host-based firewall configuration and security-log analysis through controlled Linux and Windows lab exercises.

The sessions demonstrated how firewall controls and system logs can be used together to restrict suspicious traffic, identify authentication activity, and provide security telemetry for SOC monitoring and investigation.

> **Note:** All firewall testing, authentication testing, and traffic-generation activities documented here were performed within controlled training environments.
