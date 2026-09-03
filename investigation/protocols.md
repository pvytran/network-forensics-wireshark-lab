# Protocol Analysis

## Objective

Identify the network protocols present in the PCAP and determine which protocols require additional investigation.

## Protocols Observed

| Protocol | Packets | Purpose | Suspicious? |
| -------- | ------: | ------- | ----------- |
| TBD      |     TBD | TBD     | TBD         |
| TBD      |     TBD | TBD     | TBD         |
| TBD      |     TBD | TBD     | TBD         |

## Wireshark Analysis

The following Wireshark features will be used:

* **Statistics → Protocol Hierarchy**
* **Statistics → Conversations**
* **Statistics → Endpoints**
* Display filters
* Packet inspection
* Follow Stream

## Important Protocols

### DNS

DNS traffic will be examined for:

* Unusual domains
* High-frequency queries
* Suspicious domain names
* Large or unusual DNS responses
* Possible command-and-control activity

### HTTP

HTTP traffic will be examined for:

* Requested URLs
* HTTP methods
* User-Agent strings
* Suspicious downloads
* Clear-text credentials
* Unusual HTTP responses

### TCP

TCP connections will be examined for:

* Source and destination IP addresses
* Source and destination ports
* Connection frequency
* Long-lived connections
* Unusual destinations

### TLS/HTTPS

Encrypted traffic will be reviewed for available metadata such as:

* Destination IP
* Destination port
* TLS version
* Server Name Indication (SNI), when available
* Certificate information

## Findings

> Findings will be added after analysis of the PCAP.

## Conclusion

Protocol analysis will be correlated with host and conversation analysis to identify potentially suspicious network activity.
