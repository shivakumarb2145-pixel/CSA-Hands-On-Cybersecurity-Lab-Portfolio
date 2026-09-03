# Snort IDS/IPS Detection & Blocking

## Overview

Hands-on Snort IDS/IPS exercises completed during EC-Council Certified SOC Analyst (CSA) training in a controlled virtual lab environment.

The exercises focused on network traffic monitoring, packet logging, intrusion detection, custom rule creation, alert validation, and intrusion prevention.

---

## Objectives

- Understand Snort IDS/IPS functionality
- Monitor network traffic
- Capture and log packets
- Configure Snort IDS
- Create custom detection rules
- Generate and validate security alerts
- Investigate Nmap-generated alerts
- Test intrusion prevention
- Observe traffic blocking behavior

---

## Snort Environment

Snort was installed and configured on an Ubuntu system in the lab environment.

The practical exercises covered multiple Snort operating modes:

- Sniffer mode
- Packet logging mode
- IDS mode
- IPS mode

---

## Sniffer Mode

Snort was run in sniffer mode to observe network traffic.

ICMP traffic was generated in the lab and observed through the Snort output.

This provided initial hands-on experience with:

- Network packet visibility
- Source and destination information
- Protocol identification
- Traffic monitoring

---

## Packet Logging Mode

Snort was also used in packet logging mode.

Network packets were captured and stored for further analysis.

The captured traffic was then opened and analyzed using Wireshark.

This demonstrated how Snort packet logging can support deeper network investigation.

---

## IDS Configuration

Snort IDS configuration was practiced using the Snort configuration files and rule structure.

The exercises included working with:

- Snort configuration
- Rule locations
- `HOME_NET`
- Enabled and disabled rules
- Local detection rules

Rules were managed through the local rules configuration.

---

## Nmap Detection

Controlled Nmap scanning activity was generated against the lab environment.

Snort detected the resulting network activity and generated IDS alerts.

The alerts provided visibility into suspicious scanning activity.

This demonstrated how network reconnaissance can be detected through an IDS.

---

## Custom ICMP Detection Rule

A custom ICMP detection rule was created and tested.

The rule was configured to generate an alert when the defined ICMP traffic was observed.

The rule included:

- Alert action
- ICMP protocol
- Source and destination configuration
- `HOME_NET`
- Custom message
- SID
- Revision
- Priority

The custom rule used:

```text
SID: 10000001
Revision: 1
Priority: 4

The rule was added to the local rules configuration and validated by generating ICMP traffic.

Snort successfully generated an alert for the controlled traffic.

Custom SSH Detection Rule

A custom SSH detection rule was also created.

The rule monitored TCP traffic directed toward SSH service activity.

The rule included:

Alert action
TCP protocol
Source and destination configuration
Destination port 22
Custom message
SID
Priority

The rule used:

SID: 1
Priority: 2

Controlled SSH connection attempts were generated to validate the detection.

SSH and Medusa-generated activity produced Snort alerts.

IDS Alert Validation

The custom detection rules were tested by generating controlled network activity.

The resulting alerts were reviewed to confirm that the rules were functioning as expected.

The exercises demonstrated the workflow:

Traffic Generation
       ↓
Snort Inspection
       ↓
Rule Matching
       ↓
IDS Alert
       ↓
Analyst Review
IPS Testing

Snort IPS functionality was also tested using a reject-based version of the SSH detection rule.

Snort was configured for inline operation.

A controlled SSH connection attempt was then generated.

The connection was reset/blocked by the IPS configuration.

This demonstrated the difference between:

IDS

Detect → Alert

and:

IPS

Detect → Alert → Block
Detection & Prevention Workflow

The complete exercise demonstrated a basic network detection and prevention workflow:

Network Traffic
      ↓
Snort Inspection
      ↓
Detection Rule
      ↓
Alert
      ↓
Analyst Investigation
      ↓
IPS Response
      ↓
Traffic Blocking
Connection with Wireshark

Wireshark was used alongside Snort during the training.

Snort provided IDS/IPS detection and alerting, while Wireshark provided packet-level visibility.

This combination helped connect:

Network packets
Protocol activity
Source and destination information
Detection alerts
Security investigation
SOC Analyst Perspective

Snort provided practical exposure to network-based detection.

The exercises demonstrated how a SOC analyst can:

Monitor network traffic
Identify suspicious activity
Create detection rules
Validate alerts
Investigate security events
Understand IDS versus IPS behavior
Use packet analysis to support investigation
Key Skills Practiced
Snort
IDS configuration
IPS configuration
Network traffic monitoring
Packet logging
Custom detection rules
ICMP detection
SSH detection
Nmap detection
Alert validation
Inline IPS operation
Traffic blocking
Wireshark packet analysis

Learning Outcome

Developed hands-on familiarity with Snort network intrusion detection and prevention, including traffic monitoring, packet logging, custom rule creation, alert validation, and controlled IPS blocking.

The exercises demonstrated how network-based detection can support SOC monitoring and incident investigation.

Note: All security testing and traffic-generation activities documented here were performed in controlled cybersecurity training/lab environments as part of CSA training.
