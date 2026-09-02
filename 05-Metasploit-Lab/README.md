# Metasploit Controlled Security Testing Lab

## Overview

Hands-on Metasploit Framework exercises completed during CSA training in a controlled virtual lab environment. The sessions focused on understanding vulnerability exploitation, module configuration, payload selection, Meterpreter sessions, and post-exploitation information gathering.

## Objectives

- Understand the Metasploit Framework
- Search for security-testing modules
- Review module information and options
- Configure a module for a controlled lab target
- Understand payload configuration
- Establish a Meterpreter session in the lab
- Practice basic Meterpreter commands
- Observe system and process information
- Understand post-exploitation activity from a defensive-security perspective

## Lab Environment

The exercises were performed against intentionally vulnerable lab systems.

The Metasploit exercises followed earlier reconnaissance and vulnerability-identification activities, particularly the MS17-010/SMB vulnerability lab.

The work was performed only within the controlled training environment.

## Starting Metasploit

Started the Metasploit Framework using:

```bash
msfconsole
```

## Module Search and Information

Practiced searching for relevant Metasploit modules and reviewing module information.

Used:

```text
search
info
```

The `info` command was used to examine module details and available configuration options before running a lab exercise.

## Module Configuration

Practiced configuring the required target and service options, including:

```text
RHOSTS
RPORT
```

These options were configured for the intentionally vulnerable lab target.

## Payload Configuration

Practiced selecting and configuring a suitable payload for the controlled Windows lab environment.

The session included configuring:

```text
LHOST
LPORT
```

and reviewing the required payload options before execution.

## MS17-010 Lab

The Metasploit exercise was connected to the earlier Nmap vulnerability-identification lab.

The intentionally vulnerable Windows 7 lab system was identified through the SMB vulnerability-detection exercise involving:

```text
MS17-010
EternalBlue
```

Metasploit was then used against the controlled lab target to understand how a detected vulnerability could be exploited in a training environment.

## Meterpreter Session

After successful exploitation of the controlled lab target, a Meterpreter session was obtained.

The session was used to practice basic system and process information gathering.

## Meterpreter Commands Practiced

### Help

```text
help
```

Used to review available Meterpreter commands.

### System Information

```text
sysinfo
```

Used to view information about the compromised lab system.

### User Identification

```text
getuid
```

Used to identify the user context associated with the Meterpreter session.

### Process Identification

```text
getpid
```

Used to identify the process associated with the current Meterpreter session.

### Process Listing

```text
ps
```

Used to view running processes on the lab system.

### Privilege Information

```text
getprivs
```

Used to examine available privileges within the lab session.

## Screen and Webcam Exercises

The training session also included controlled demonstrations of Meterpreter capabilities related to screen and webcam access:

```text
screenshot
webcam_snap
webcam_stream
screenshare
```

These exercises were performed within the isolated training environment to understand the types of endpoint activity that security monitoring solutions may need to detect.

## Security Monitoring Perspective

The practical exercises demonstrated why post-exploitation activity can generate valuable security telemetry.

Potential defensive investigation areas include:

- Unexpected process creation
- Unusual user activity
- Suspicious network connections
- Unexpected privilege usage
- Remote access activity
- Endpoint process behavior

These concepts were later connected with Windows logs, Sysmon, Wazuh, SIEM monitoring, and incident investigation during the CSA training.

## Relationship to SOC Operations

The lab demonstrated the relationship between offensive activity and defensive monitoring:

```text
Vulnerability Identification
          ↓
Controlled Exploitation
          ↓
Meterpreter Session
          ↓
System / Process Activity
          ↓
Security Telemetry
          ↓
Detection & Investigation
```

Understanding how attacks generate telemetry helped provide context for later SOC-focused exercises involving SIEM, endpoint monitoring, IDS/IPS, and incident response.

## Key Skills Practiced

- Metasploit Framework
- Module discovery
- Module information analysis
- Target configuration
- Payload configuration
- Meterpreter
- System information gathering
- Process investigation
- Privilege inspection
- Controlled vulnerability exploitation
- Defensive understanding of post-exploitation activity

## Learning Outcome
Developed practical familiarity with the Metasploit Framework and Meterpreter through controlled cybersecurity lab exercises.

The exercises helped connect vulnerability identification with exploitation and demonstrated the types of endpoint and network activity that can subsequently be investigated by a SOC analyst.

> **Note:** All exploitation and post-exploitation activities documented here were performed against controlled training targets and intentionally vulnerable lab systems.
