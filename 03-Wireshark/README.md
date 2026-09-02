# Wireshark Network Traffic Analysis

## Overview

Hands-on Wireshark exercises completed during CSA training. The sessions focused on capturing, filtering, and analyzing network traffic generated in controlled lab environments.

## Objectives

- Capture network traffic
- Identify source and destination information
- Analyze network protocols
- Understand ICMP request and reply traffic
- Analyze TCP connections and the three-way handshake
- Inspect HTTP requests and responses
- Analyze Netcat communication
- Observe Nmap-generated traffic
- Save and reopen packet captures
- Use display and capture filters

## Traffic Generation

Traffic was generated from the Kali Linux lab environment by:

- Pinging a domain
- Pinging an IP address
- Visiting websites
- Establishing Netcat communication
- Performing controlled Nmap activity

The generated traffic was captured and analyzed using Wireshark.

## Packet Capture Analysis

After capturing traffic, examined:

- Packet time
- Source IP
- Destination IP
- Protocol
- Packet length

The packet list, packet details, and packet bytes panes were used to examine individual packets.

## ICMP Analysis

Captured and analyzed ICMP traffic generated through ping activity.

Observed:

```text
ICMP Echo Request
        ↓
ICMP Echo Reply

This helped identify the communication between the source and destination hosts.

Display filter practiced:

icmp
TCP Analysis

Analyzed TCP traffic and observed the TCP three-way handshake:

Client                    Server

   SYN  -------------------->
        <---------------- SYN-ACK
   ACK  -------------------->

Examined source and destination IP addresses and ports during TCP communication.

Display filter:

tcp
HTTP Traffic Analysis

Generated HTTP traffic by visiting websites and analyzed the resulting packets.

Observed:

HTTP GET requests
Source and destination IP addresses
Source and destination ports
HTTP response status
TCP communication underlying HTTP

Display filters practiced:

http
http.request.method==GET
tcp.port==80

Observed successful HTTP responses including:

200

Used Follow TCP Stream to inspect the communication associated with an HTTP connection.

Netcat Traffic Analysis

Performed a controlled Netcat communication exercise between lab machines.

Kali was configured as a listener:

nc -lvp 2323

A second machine connected to the listener and exchanged messages.

Wireshark was then used to identify and inspect the traffic:

tcp.port==2323

Used Follow TCP Stream to examine the exchanged communication.

Nmap Traffic Observation

Observed network traffic generated during controlled Nmap host discovery and scanning exercises.

Wireshark was used to examine the packets associated with the scanning activity and understand how network scanning traffic appears at the packet level.

Display Filters Practiced

The following Wireshark display filters were practiced:

icmp
http
http.request.method==GET
tcp
udp
ip.addr=ipaddress
tcp.port==80
tcp.port==2323

These filters were used to narrow packet views during traffic analysis.

Capture Filters

Practiced capture filtering for specific traffic including:

ICMP
UDP
Specific hosts
Source IP addresses
Destination IP addresses
Port 80 traffic

Capture filters were used to limit the traffic collected during packet capture.

Packet Capture Files

Captured traffic was saved as .pcap files and later reopened in Wireshark for analysis.

The saved captures were used to review previously generated network activity.

Wireshark Interface

Worked with the three primary packet-analysis areas:

Packet List
Packet Details
Packet Bytes

Also practiced:

Coloring rules
Adding packet-list columns
Removing columns
Examining individual packet fields
Key Observations

The exercises demonstrated how common activities appear at the packet level, including:

ICMP ping requests and replies
TCP connection establishment
HTTP GET requests
HTTP responses
Netcat communication
Network scanning traffic

Learning Outcome

Developed practical experience capturing and analyzing network traffic with Wireshark and using packet-level evidence
to understand communication between systems.
The Wireshark exercises provided a foundation for later network-security activities involving Nmap, Snort IDS/IPS,
firewalls, and SIEM-based investigation.
ICMP Echo Request
        ↓
ICMP Echo Reply
