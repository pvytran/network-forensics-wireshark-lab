# Network Forensics — Wireshark PCAP Investigation

## Overview

This project documents a network forensics investigation using **Wireshark** to analyze packet capture (PCAP) data.

The goal of the investigation is to identify hosts, protocols, network conversations, suspicious traffic, and indicators of compromise (IOCs).

## Investigation Workflow

```text
PCAP
 ↓
Identify Hosts
 ↓
Identify Protocols
 ↓
Analyze Conversations
 ↓
Investigate Suspicious Traffic
 ↓
Extract Indicators
 ↓
Document Findings
```

## Tools Used

* Wireshark
* TShark
* Windows 10
* PCAP/PCAPNG files

## Objectives

The investigation focuses on:

* Identifying communicating hosts
* Identifying commonly used network protocols
* Examining TCP and UDP conversations
* Following suspicious network streams
* Investigating DNS, HTTP, TLS, and other relevant traffic
* Identifying potentially malicious activity
* Extracting IP addresses, domains, URLs, and other indicators
* Documenting the investigation and findings

## Environment

| Component        | Details           |
| ---------------- | ----------------- |
| Operating System | Windows 10        |
| Primary Tool     | Wireshark         |
| Additional Tool  | TShark            |
| Evidence         | PCAP/PCAPNG       |
| Analysis Type    | Network Forensics |

## Investigation

### 1. Host Identification

The first stage of the investigation identifies the hosts communicating within the captured traffic.

Evidence and screenshots will be documented in:

`investigation/hosts.md`

### 2. Protocol Analysis

Network protocols observed in the capture will be reviewed to determine normal and potentially suspicious communications.

Examples include:

* DNS
* HTTP
* HTTPS/TLS
* TCP
* UDP
* ICMP

Evidence will be documented in:

`investigation/protocols.md`

### 3. Conversation Analysis

Network conversations will be examined to identify:

* Source and destination IP addresses
* Ports
* Connection frequency
* Data transfers
* Unusual communication patterns

Evidence will be documented in:

`investigation/conversations.md`

### 4. Suspicious Traffic

Potentially suspicious traffic will be investigated using Wireshark filters, stream reconstruction, packet inspection, and other forensic techniques.

Examples of areas investigated:

* Unusual DNS requests
* Suspicious HTTP requests
* Unexpected external connections
* Repeated connections to the same host
* Possible command-and-control traffic
* Possible data transfer or exfiltration

### 5. Indicators of Compromise

Relevant indicators identified during the investigation will be documented, including:

* IP addresses
* Domains
* URLs
* Ports
* Protocols
* File hashes, when available
* Other relevant network artifacts

Indicators will be documented in:

`investigation/indicators.md`

## Findings

> Findings will be added as the PCAP investigation is completed.

## Screenshots

Screenshots demonstrating the investigation process will be stored in:

```text
screenshots/
```

Examples include:

* Wireshark packet overview
* Protocol hierarchy
* Conversations
* Endpoints
* Follow TCP Stream
* DNS investigation
* HTTP investigation
* Suspicious traffic

## Final Report

A complete investigation report will be maintained in:

`report/investigation-report.md`

The final report will summarize:

1. Investigation scope
2. Evidence examined
3. Hosts identified
4. Protocols identified
5. Suspicious activity
6. Indicators of compromise
7. Findings
8. Analyst conclusion

## Disclaimer

This project is intended for educational and cybersecurity portfolio purposes. Analysis is performed on authorized laboratory PCAP data.
