# Incident Response, Jira & SOAR Lab

## Overview

Hands-on incident response and security operations exercises completed during CSA training. The sessions focused on incident response processes, security playbooks, Jira-based task management, and SOAR concepts.

## Objectives

- Understand incident response
- Learn the incident response lifecycle
- Understand security incident preparation
- Practice detection and analysis concepts
- Understand containment, eradication, and recovery
- Understand post-incident activities
- Study incident response playbooks
- Use Jira for security task management
- Understand SOAR concepts
- Understand SOAR playbooks
- Connect incident response with SOC monitoring and investigation

## Incident Response

Incident response was studied as the process of managing security incidents from initial detection through recovery and post-incident activities.

The training covered the importance of:

- Identifying security incidents
- Collecting relevant information
- Analyzing security events
- Containing malicious or suspicious activity
- Removing the cause of an incident
- Recovering affected systems
- Documenting lessons learned

## Incident Response Lifecycle

The following incident response lifecycle was studied:

```text
Preparation
     ↓
Detection & Analysis
     ↓
Containment
     ↓
Eradication
     ↓
Recovery
     ↓
Post-Incident Activity
```

Each stage was studied as part of the overall incident response process.

## Preparation

Preparation focuses on ensuring that an organization has the appropriate processes, tools, procedures, and resources available before an incident occurs.

The sessions introduced the importance of:

- Security procedures
- Incident response plans
- Playbooks
- Monitoring capabilities
- Security tools
- Documentation

## Detection & Analysis

The detection and analysis stage focuses on identifying suspicious activity and determining whether a security incident has occurred.

The CSA training connected this stage with the SIEM and endpoint-security exercises performed using:

- IBM QRadar
- Splunk
- Wazuh
- Snort
- Windows Event Logs
- Sysmon
- Wireshark

Security events can be correlated to understand the scope and progression of suspicious activity.

## Containment

Containment focuses on limiting the impact and spread of a security incident.

The training introduced containment as an important step following detection and analysis.

Examples of security controls practiced during the CSA labs included:

- Firewall traffic restrictions
- SSH access restrictions
- Snort IPS blocking
- Endpoint monitoring

These exercises demonstrated how security controls can be used to limit suspicious activity in a controlled environment.

## Eradication

Eradication focuses on removing the cause or artifacts associated with a security incident.

The training covered eradication as part of the incident response lifecycle.

Security analysis and endpoint investigation can help identify the source of malicious or suspicious activity before remediation.

## Recovery

Recovery focuses on restoring affected systems and services to normal operation after an incident has been contained and addressed.

The training covered recovery as a stage of the incident response lifecycle.

## Post-Incident Activity

Post-incident activities focus on reviewing what happened, documenting findings, identifying lessons learned, and improving future security processes.

The importance of documentation and continuous improvement was emphasized during the incident response training.

## Incident Response Playbooks

Studied incident response playbooks as structured procedures for handling recurring security incidents.

Playbooks can provide analysts with defined steps for:

- Investigation
- Containment
- Remediation
- Recovery
- Documentation
- Escalation

Playbooks help security teams maintain a consistent response process.

## Jira

Jira was introduced as a platform for managing security-related tasks and workflows.

The exercises included:

- Creating a Jira account
- Creating a team
- Creating a space
- Creating tasks
- Assigning tasks

## Security Task Management

Jira was used to understand how security work can be organized and assigned.

A simplified workflow can be represented as:

```text
Security Issue
      ↓
Create Task
      ↓
Assign Task
      ↓
Investigation / Remediation
      ↓
Track Progress
      ↓
Complete Task
```

This provides a structured approach for tracking security-related work.

## SOAR

Studied Security Orchestration, Automation and Response (SOAR) concepts.

The training introduced the use of automation and orchestration to support security operations.

SOAR concepts covered included:

- Security automation
- Workflow orchestration
- Response playbooks
- Alert handling
- Repetitive task automation
- Security-tool integration

## SOAR Playbooks

Studied SOAR playbooks as automated or semi-automated workflows that can help security teams respond to alerts consistently.

A generalized workflow can be represented as:

```text
Security Alert
      ↓
Trigger
      ↓
Automated / Manual Investigation
      ↓
Response Action
      ↓
Documentation
      ↓
Closure
```

## Connection with SOC Operations

Incident response concepts were connected with the hands-on SOC exercises performed throughout the CSA training.

A broader SOC workflow was studied through:

```text
Security Telemetry
      ↓
Detection
      ↓
Alert / Offense
      ↓
Investigation
      ↓
Incident Identification
      ↓
Containment
      ↓
Remediation
      ↓
Recovery
      ↓
Documentation
      ↓
Lessons Learned
```

## Practical Incident Investigation

The QRadar exercises provided practical exposure to incident investigation and documentation.

A simulated multi-stage incident was investigated involving:

- Multiple authentication failures
- Successful SSH authentication
- Privilege escalation
- Root-level activity
- Python HTTP server activity
- Port 8000 network activity
- `confidential.txt` activity
- A different source IP

The investigation involved correlating authentication and network activity, building a timeline, documenting findings, and identifying the need for further investigation and escalation.

## SOC Analyst Perspective

Incident response requires analysts to combine security telemetry from multiple sources.

During the CSA training, this included working with:

- SIEM events
- Network traffic
- Authentication logs
- Endpoint telemetry
- Firewall logs
- IDS/IPS alerts
- Threat intelligence
- File-integrity events

The information can be correlated to understand what occurred and support appropriate response actions.

## Key Skills Practiced

- Incident response lifecycle
- Incident detection and analysis
- Security playbooks
- Incident documentation
- Security investigation
- Jira
- Security task management
- SOAR concepts
- SOAR playbooks
- Alert handling
- Security workflow
- Incident escalation
- SOC operations

## Learning Outcome

Developed practical understanding of incident response processes, security playbooks, task management, and SOAR concepts through CSA training.

The exercises also demonstrated how SIEM, endpoint, network, and threat-intelligence information can support the detection, investigation, documentation, and response stages of a security incident.

> **Note:** The incident scenarios and security activities documented in this section were performed or studied within controlled cybersecurity training environments.
