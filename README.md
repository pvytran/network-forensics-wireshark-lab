# Network Forensics Investigation — Wireshark

## Overview

This project demonstrates a controlled network-forensics investigation using Wireshark, tcpdump, and Scapy.

The investigation analyzes simulated network traffic to identify suspicious HTTP activity, reconstruct network communications, extract indicators of compromise (IOCs), and document an incident timeline.

## Objectives

- Analyze PCAP network traffic
- Identify communicating hosts
- Investigate DNS activity
- Analyze HTTP requests and responses
- Identify suspicious file-download activity
- Investigate TCP communications
- Extract network indicators of compromise
- Build an incident timeline
- Produce a SOC-style investigation report

## Lab Environment

**Operating System:** Kali Linux

**Tools:**

- Wireshark
- tcpdump
- Scapy

## Network Hosts

| Role | IP Address |
|---|---|
| Victim Workstation | `192.168.56.105` |
| Simulated Server | `192.168.56.200` |
| DNS Server | `192.168.56.1` |

## Investigation Findings

### Finding 1 — Suspicious File Download

The workstation `192.168.56.105` requested:

```text
GET /download/update.exe

from 
192.168.56.200

over HTTP port 80.

Finding 2 — Server Response

The server returned:

HTTP/1.1 200 OK

with:

Content-Type: application/octet-stream

indicating that binary/file data was returned.

Finding 3 — Simulated C2 Check-In

The workstation communicated with the simulated server over TCP port 8080.

The HTTP request contained:

POST /api/checkin

with simulated workstation status information.

Indicators of Compromise
Type	Indicator
IP Address	192.168.56.200
Host	update-server.local
URI	/download/update.exe
URI	/api/checkin
Port	80
Port	8080

Investigation Methodology

PCAP
  ↓
Traffic Filtering
  ↓
Host Identification
  ↓
DNS Analysis
  ↓
HTTP Analysis
  ↓
TCP Analysis
  ↓
IOC Extraction
  ↓
Timeline Reconstruction
  ↓
SOC Investigation Report


Skills Demonstrated
Network Forensics
Wireshark
PCAP Analysis
TCP/IP Analysis
DNS Analysis
HTTP Analysis
tcpdump
Scapy
IOC Identification
Incident Investigation
SOC Documentation
Disclaimer

This project uses simulated network traffic in a controlled laboratory environment for educational and portfolio purposes. No real malware or unauthorized systems were used.
