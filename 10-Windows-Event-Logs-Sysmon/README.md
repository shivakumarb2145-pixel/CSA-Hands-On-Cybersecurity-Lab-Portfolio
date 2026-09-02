# Windows Event Logs & Sysmon Analysis Lab

## Overview

Hands-on Windows security monitoring exercises completed during CSA training in a controlled virtual lab environment. The sessions focused on Windows Event Viewer, security event analysis, authentication activity, account management events, and Sysmon telemetry.

## Objectives

- Understand Windows Event Viewer
- Explore Windows event log categories
- Analyze Windows Security events
- Identify important Windows Event IDs
- Investigate successful and failed authentication activity
- Understand user account-related events
- Configure and use Sysmon
- Analyze Sysmon Operational logs
- Identify process, network, file, and other endpoint activity

## Lab Environment

The exercises were performed in a controlled virtual Windows environment using Windows Event Viewer and Sysmon.

## Windows Event Viewer

Used Windows Event Viewer to inspect system and security-related logs.

The main log categories reviewed included:

- Application
- Security
- Setup
- System
- Forwarded Events

Event Viewer was used to review timestamps, event IDs, event descriptions, and other available event information.

## Important Windows Security Event IDs

The following Windows Event IDs were studied during the exercises:

| Event ID | Activity |
|----------|----------|
| 104 | Event log cleared |
| 1102 | Security audit log cleared |
| 4624 | Successful account logon |
| 4625 | Failed account logon |
| 4634 | Account logoff |
| 4647 | User-initiated logoff |
| 4720 | User account created |
| 4722 | User account enabled |
| 4725 | User account disabled |
| 4726 | User account deleted |

These events were reviewed to understand how authentication and account-management activity can appear in Windows security logs.

## Authentication Monitoring

Analyzed Windows authentication events to understand the difference between successful and failed login activity.

Examples included:

- Successful logons
- Failed logons
- Logoff activity
- Repeated authentication failures

This type of telemetry can help identify suspicious authentication behavior such as repeated failed login attempts.

## User Account Monitoring

Reviewed account-management events related to:

- User creation
- User enablement
- User disablement
- User deletion

These events are important when investigating unexpected changes to Windows accounts.

## Sysmon

Installed and configured Sysmon to generate detailed Windows endpoint telemetry.

Sysmon logs were accessed through:

**Applications and Services Logs → Microsoft → Windows → Sysmon → Operational**

The Sysmon Operational log was reviewed to understand endpoint activity beyond the standard Windows event logs.

## Sysmon Event IDs Practiced

The following Sysmon events were studied:

| Event ID | Activity |
|----------|----------|
| 1 | Process creation |
| 3 | Network connection |
| 10 | Process access |
| 11 | File creation |
| 15 | File creation stream hash |
| 22 | DNS query |
| 23 | File deletion |

These events provide additional visibility into processes, network connections, files, DNS activity, and process-access behavior.

## Endpoint Investigation

Sysmon telemetry was used to understand how endpoint activity can be investigated by a security analyst.

Examples of useful telemetry included:

- Process creation
- Network connections
- File activity
- DNS queries
- Process access
- File deletion

Combining these events can help establish a timeline of suspicious endpoint activity.

## SOC Investigation Relevance

Windows Event Logs and Sysmon provide valuable telemetry for SOC monitoring and investigation.

A security analyst can correlate:

1. Authentication activity
2. Process creation
3. Network connections
4. File activity
5. DNS activity
6. Account changes

This can help identify suspicious behavior and support incident investigation.

## Key Skills Practiced

- Windows Event Viewer
- Windows Security Logs
- Windows Event IDs
- Authentication monitoring
- Account activity analysis
- Sysmon
- Sysmon Operational logs
- Process monitoring
- Network connection monitoring
- File activity monitoring
- Endpoint telemetry analysis
- Security event investigation

## Learning Outcome

Developed practical familiarity with Windows security logging and Sysmon endpoint telemetry through controlled cybersecurity lab exercises.

The exercises demonstrated how Windows event data can be used to investigate authentication activity, account changes, processes, network connections, and other endpoint behaviors relevant to SOC operations.

> **Note:** All Windows monitoring and security analysis activities documented here were performed in controlled training environments.
