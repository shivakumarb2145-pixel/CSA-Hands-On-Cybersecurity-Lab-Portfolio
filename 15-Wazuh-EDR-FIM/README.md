# Wazuh EDR & File Integrity Monitoring Lab

## Overview

Hands-on endpoint security and incident response exercises completed during CSA training using Wazuh in a controlled virtual lab environment. 
The sessions focused on endpoint monitoring, agent deployment, file integrity monitoring, authentication monitoring, suspicious process detection, and security operations workflows.

## Objectives

- Understand endpoint security concepts
- Understand EDR and XDR capabilities
- Deploy and configure Wazuh agents
- Monitor Linux endpoints
- Monitor Windows endpoints
- Perform File Integrity Monitoring (FIM)
- Detect file creation, modification, and deletion
- Monitor authentication failures
- Identify suspicious processes and network listeners
- Understand incident response workflows
- Understand security playbooks
- Learn Jira-based security task management
- Understand SOAR and security automation concepts

## Lab Environment

The exercises were performed in a controlled virtual lab environment using:

- Wazuh Server
- Kali Linux endpoint
- Windows endpoint
- Jira
- Controlled security-testing activities

## Wazuh

Wazuh was studied as an endpoint security platform for monitoring endpoint activity and identifying security events.

The practical exercises included:

- Wazuh server access
- Agent deployment
- Endpoint monitoring
- Security event collection
- File Integrity Monitoring
- Authentication monitoring
- Process and network activity monitoring

## Agent Deployment

A Wazuh agent was deployed on a Kali Linux endpoint and connected to the Wazuh server.

The workflow was:

```text
Wazuh Server
      ↓
Deploy Agent
      ↓
Connect Endpoint
      ↓
Generate Security Activity
      ↓
Collect Events
      ↓
Monitor & Investigate

A Windows endpoint was also configured with a Wazuh agent for endpoint monitoring.

File Integrity Monitoring

File Integrity Monitoring (FIM) was practiced on both Linux and Windows endpoints.

The exercises included:

Creating files
Modifying files
Deleting files
Monitoring file changes
Reviewing Wazuh alerts and event information
Linux FIM

On the Kali Linux endpoint, files were created, modified, and deleted while Wazuh monitored the changes.

The observed activities included:

File Created
     ↓
File Modified
     ↓
File Deleted
     ↓
Wazuh FIM Event
     ↓
Event Investigation
Windows FIM

Similar file integrity exercises were performed on the Windows endpoint.

File creation, modification, and deletion activities were monitored through the Wazuh agent.

Authentication Monitoring

Controlled SSH authentication testing was performed against the Kali Linux endpoint.

Hydra was used within the lab environment to generate repeated authentication failures.

Wazuh collected and displayed the resulting authentication events.

The investigation workflow was:

Authentication Attempts
        ↓
Failed Login Events
        ↓
Wazuh Detection
        ↓
Review Source Information
        ↓
Investigate Activity

This demonstrated how endpoint telemetry can help identify password-attack activity.

Suspicious Process & Network Listener Detection

An unauthorized network listener was created in the controlled lab using Netcat.

Wazuh was used to observe information associated with the process and network listener.

The exercise demonstrated how endpoint monitoring can help analysts identify unexpected processes
and listening services.

Endpoint Detection & Response

The exercises demonstrated how endpoint telemetry can support detection and investigation.

Relevant endpoint information included:

File activity
Authentication events
Processes
Network listeners
Endpoint changes
Security alerts

This information can help a SOC analyst investigate suspicious endpoint behaviour and correlate activity
with other security telemetry.

Incident Response

Incident response concepts were studied using the following lifecycle:

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

The exercises emphasized the importance of collecting evidence, analyzing security events, documenting incidents,
and following appropriate response procedures.

Incident Response Playbooks

Playbooks were studied as structured procedures that help security teams respond
consistently to common security incidents.

Examples of activities that can be supported by playbooks include:

Authentication attacks
Malware incidents
Suspicious endpoint activity
Unauthorized processes
Data security incidents
Jira Security Workflow

Jira was introduced as a platform for security task and incident management.

The exercises included:

Creating a Jira account
Creating a team
Creating a workspace/space
Creating tasks
Assigning tasks
Understanding security workflow management

Jira can support SOC operations by helping teams track investigation tasks, remediation activities,
and incident-related work.

SOAR

Security Orchestration, Automation and Response (SOAR) concepts were studied.

The exercises introduced:

Security workflow automation
Playbook-based response
Alert handling
Task automation
Integration between security tools

SOAR can help security teams standardize repetitive response processes and improve operational efficiency.

SOC Investigation Workflow

The Wazuh exercises were connected to a broader SOC investigation workflow:

Endpoint Activity
       ↓
Security Event
       ↓
Detection
       ↓
Alert Review
       ↓
Investigation
       ↓
Incident Documentation
       ↓
Response / Escalation
SOC Relevance

Wazuh endpoint monitoring can support SOC analysts by helping them:

Monitor endpoint activity
Investigate authentication failures
Detect file changes
Identify suspicious processes
Investigate network listeners
Collect endpoint telemetry
Support incident response
Document security investigations

Learning Outcome

Developed practical familiarity with Wazuh endpoint monitoring, agent deployment, File Integrity Monitoring,
authentication-event investigation, suspicious process and network-listener detection, and incident response workflows.
The exercises also provided exposure to Jira-based security task management and SOAR playbook concepts, strengthening understanding
of how endpoint telemetry fits into SOC operations.
