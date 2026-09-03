# Network Forensics Investigation Report

## Executive Summary

A controlled network-forensics investigation was performed using Wireshark against a simulated PCAP.

The investigation identified suspicious HTTP activity originating from workstation `192.168.56.105`.

The workstation requested `/download/update.exe` from `192.168.56.200` and subsequently generated a simulated check-in request to the same server over TCP port `8080`.

## Affected Host

- Victim IP: `192.168.56.105`

## Investigated Server

- Server IP: `192.168.56.200`
- Hostname: `update-server.local`

## Findings

### Finding 1 — Suspicious File Download

The workstation issued:

`GET /download/update.exe`

over HTTP to `192.168.56.200`.

### Finding 2 — Successful Server Response

The server returned:

`HTTP/1.1 200 OK`

with:

`Content-Type: application/octet-stream`

### Finding 3 — Simulated C2 Check-In

The workstation subsequently communicated with the server over TCP port `8080` using:

`POST /api/checkin`

The request contained simulated workstation status information.

## Timeline

1. Workstation performed DNS activity.
2. Workstation established normal HTTP communication.
3. Workstation requested `/download/update.exe`.
4. Server returned HTTP `200 OK`.
5. Workstation connected to TCP port `8080`.
6. Workstation sent `/api/checkin`.

## Analyst Assessment

The traffic demonstrates characteristics that a SOC analyst should investigate further, including a suspicious executable download followed by application-level check-in traffic.

Because this is a controlled simulation, the activity should not be interpreted as evidence of a real-world compromise.

## Tools

- Wireshark
- tcpdump
- Scapy
- Kali Linux

## Evidence

Wireshark screenshots documenting the investigation are stored in the `screenshots` directory.

## Disclaimer

This investigation was performed in a controlled laboratory environment using simulated network traffic for cybersecurity education and portfolio development.
