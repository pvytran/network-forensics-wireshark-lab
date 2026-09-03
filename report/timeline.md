# Investigation Timeline

## Overview

This timeline documents the sequence of activities performed during the network forensics investigation.

| Step | Activity                             | Evidence                   | Status   |
| ---- | ------------------------------------ | -------------------------- | -------- |
| 1    | Loaded PCAP into Wireshark           | PCAP file                  | Complete |
| 2    | Searched for `update.exe`            | 01-suspicious-download.png | Complete |
| 3    | Identified network endpoints         | 02-host-identification.png | Complete |
| 4    | Reviewed protocol hierarchy          | 03-protocol-hierarchy.png  | Complete |
| 5    | Reconstructed TCP conversation       | 04-follow-tcp-stream.png   | Complete |
| 6    | Examined HTTP response               | 05-http-response.png       | Complete |
| 7    | Identified suspicious host and ports | 06-suspicious-host.png     | Complete |
| 8    | Extracted confirmed IOCs             | indicators.md              | Pending  |
| 9    | Completed final assessment           | investigation-report.md    | Pending  |

## Event Sequence

### Initial Analysis

The PCAP was loaded into Wireshark and examined to establish an overview of the captured network activity.

### Suspicious Request

An HTTP request matching:

```text
http.request.uri contains "update.exe"
```

was identified for further investigation.

### Host Analysis

Network endpoints were reviewed to identify the systems participating in the communication.

### Conversation Reconstruction

The relevant TCP conversation was reconstructed using Wireshark's **Follow TCP Stream** functionality.

### HTTP Analysis

The HTTP request and response were examined for additional evidence related to the downloaded file.

### IOC Extraction

Confirmed IP addresses, domains, URLs, ports, and other relevant artifacts will be recorded after the PCAP evidence is reviewed in detail.

## Current Status

The investigation remains **in progress**.

The final determination of whether the observed `update.exe` activity is malicious will be based on additional analysis of the PCAP.
