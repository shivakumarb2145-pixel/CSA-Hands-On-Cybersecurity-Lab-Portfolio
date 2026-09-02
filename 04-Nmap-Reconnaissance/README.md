# Nmap & Network Reconnaissance

## Overview

Hands-on network reconnaissance and scanning exercises completed during CSA training in controlled lab environments. The sessions focused on host discovery, port scanning, service identification, Nmap scripting, and vulnerability identification.

## Objectives

- Identify active hosts on a lab network
- Understand different host-discovery techniques
- Perform TCP port scanning
- Compare TCP connect and SYN scanning
- Scan all TCP ports
- Identify services and versions
- Use Nmap NSE scripts
- Observe scanning traffic using Wireshark
- Identify a known SMB vulnerability in a controlled lab

## Lab Environment

The exercises were performed in a controlled virtual lab environment using Kali Linux and intentionally vulnerable or test systems.

Network information was first identified using:

```bash
ifconfig

The discovered network range was then used for controlled host-discovery exercises.

Host Discovery with fping

Used fping to identify active hosts within the lab network range.

Example:

fping -aqg iprange

The resulting traffic was observed in Wireshark to understand how host discovery generated ICMP traffic.

Nmap Host Discovery

Practiced Nmap host discovery using:

nmap -sn ipaddress-254

The exercise demonstrated how Nmap can identify hosts without performing a traditional port scan.

The generated traffic was observed in Wireshark.

ARP Host Discovery

Practiced ARP-based host discovery using:

sudo nmap -sn iprange

MAC address information was observed for hosts discovered through the local network.

TCP Connect Scan

Performed a TCP connect scan using:

nmap -sT ip/domain

This was used to identify accessible TCP ports on the lab target.

SYN Scan

Practiced a TCP SYN/half-open scan:

nmap -sS ip

The exercise helped demonstrate how SYN scanning differs from a full TCP connection.

Scanning All Ports

Practiced scanning the full TCP port range using:

nmap -p- ip

This was used to identify services that might be running on ports outside commonly scanned ports.

Service and Version Detection

Used:

nmap -sV ip

to identify services and their versions running on discovered ports.

The identified service information was used during later vulnerability-analysis exercises.

Aggressive Scan

Practiced Nmap aggressive scanning:

sudo nmap -A ip

This exercise demonstrated additional information that Nmap can collect through service detection and Nmap scripts.

Nmap NSE Scripts

Explored the Nmap scripting engine and available scripts under:

/usr/share/nmap/scripts/

Also practiced viewing script information using:

sudo nmap --script-help scriptname
SMB Vulnerability Detection

Used the Nmap SMB vulnerability detection script:

smb-vuln-ms17-010.nse

The lab target was scanned for the SMB vulnerability associated with MS17-010.

The exercise identified a vulnerable Windows 7 lab system.

The vulnerability was studied in relation to EternalBlue and its associated CVE.

Controlled Vulnerability Lab

Following vulnerability identification, the lab continued with controlled exploitation exercises using the Metasploit Framework against the intentionally vulnerable Windows lab system.

The activity was performed within the training environment to understand the relationship between:

Reconnaissance
      ↓
Service Identification
      ↓
Vulnerability Detection
      ↓
Controlled Exploitation
      ↓
Security Monitoring
Wireshark Correlation

Nmap-generated network traffic was observed using Wireshark.

This helped connect reconnaissance techniques with the network-level traffic they produce.

Key Skills Practiced
Network host discovery
ICMP-based discovery
ARP discovery
TCP port scanning
SYN scanning
Service/version enumeration
Nmap NSE
SMB vulnerability identification
Network traffic observation
Vulnerability analysis in controlled environments

Learning Outcome

Developed practical understanding of network reconnaissance and how different Nmap scanning techniques identify hosts,
ports, services, and vulnerabilities.
The exercises also demonstrated how reconnaissance activity can be observed at the packet level and later used as
security telemetry for detection and investigation.
