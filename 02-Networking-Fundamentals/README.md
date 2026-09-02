# Networking Fundamentals

## Overview

Hands-on networking exercises completed during CSA training. The sessions focused on understanding network communication, addressing, protocols, ports, TCP connections, HTTP, and basic network security concepts.

## Topics Practiced

- Packets, headers, and payloads
- Network Interface Cards (NICs)
- MAC addresses
- Hubs, switches, and routers
- Hostnames
- IPv4 and IPv6 addressing
- Private and public IP addresses
- Network Address Translation (NAT)
- TCP and UDP
- TCP three-way handshake
- Network ports
- Source and destination ports
- Netcat communication
- HTTP methods and status codes
- Metasploitable 2 lab environment
- Network threat categories

## Packets

Studied how network communication is divided into packets and examined the role of:

- Headers
- Payloads
- Source and destination information
- Network protocols

## MAC Addresses and NICs

Learned about Network Interface Cards (NICs) and MAC addresses used for network communication.

MAC addresses were studied as hardware-level addresses associated with network interfaces.

## Network Devices

Studied the basic roles of:

- Hubs
- Switches
- Routers

These devices were used to understand how traffic moves between hosts and networks.

## IP Addressing

Practiced understanding:

- Hostnames
- IPv4 addresses
- IPv6 addresses
- Private IP addresses
- Public IP addresses
- Network Address Translation (NAT)

IPv4 was studied as a 32-bit addressing system and IPv6 as a 128-bit addressing system.

## TCP and UDP

Studied the differences between TCP and UDP.

### TCP

TCP provides connection-oriented communication.

Practiced understanding the TCP three-way handshake:

```text
Client                    Server

   SYN  -------------------->
        <---------------- SYN-ACK
   ACK  -------------------->

UDP

UDP was studied as a connectionless transport protocol.

Network Ports

Studied logical network ports and source/destination port concepts.

Examples covered during training included:

Protocol	Port
FTP	20/21
Telnet	23
SMTP	25
DNS	53
HTTP	80

Studied how source and destination ports identify communication endpoints.

Netcat Lab

Practiced basic client-server communication using Netcat in a controlled lab environment.

Listener example:

nc -lvp 2323

A second machine connected to the listener and exchanged messages.

The resulting traffic was later inspected using Wireshark.

HTTP

Studied HTTP communication and common HTTP methods:

GET
POST
PUT
DELETE

Also studied HTTP response status codes including:

200
404
500

The sessions included observing HTTP requests and responses and understanding how HTTP operates over TCP.

Metasploitable 2

Set up the Metasploitable 2 intentionally vulnerable virtual machine in VirtualBox for controlled cybersecurity lab exercises.

The environment was used as a target for later security testing and network-security exercises.

Network Threat Categories

Studied several broad categories of network and system threats:

Network Threats

Examples included:

Denial of Service (DoS)
Distributed Denial of Service (DDoS)
Host Threats

Focused on threats involving malware and exploitation of host systems.

Web Application Threats

Studied threats affecting web applications, including:

Website defacement
SQL injection

Learning Outcome

Developed practical understanding of how hosts communicate across networks, how TCP and UDP differ,
how IP addresses and ports identify communication endpoints, and how common protocols such as HTTP operate.

These networking fundamentals were later applied during Wireshark analysis, Nmap scanning, firewall configuration,
IDS/IPS monitoring, and SIEM investigations.
