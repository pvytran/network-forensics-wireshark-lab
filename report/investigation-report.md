# Network Forensics Investigation Report

## 1. Executive Summary

This report documents a network forensics investigation performed using Wireshark against an authorized PCAP dataset.

The investigation focused on identifying communicating hosts, protocols, network conversations, suspicious activity, and potential indicators of compromise.

## 2. Scope

The investigation covered:

* Network hosts
* Network protocols
* TCP/UDP conversations
* DNS activity
* HTTP activity
* TLS/HTTPS metadata
* Suspicious network connections
* Potential indicators of compromise

## 3. Tools

* Wireshark
* TShark
* Windows 10

## 4. Host Analysis

### Key Hosts

> Add confirmed hosts and their roles here.

### Observations

> Document important host-to-host communication.

## 5. Protocol Analysis

### Protocols Observed

> Add the protocols identified from Wireshark's Protocol Hierarchy.

### Observations

> Describe any unusual or noteworthy protocol activity.

## 6. Conversation Analysis

> Document important conversations discovered through Wireshark's Conversations feature.

Include:

* Source IP
* Destination IP
* Source port
* Destination port
* Protocol
* Packet/byte counts
* Duration

## 7. Suspicious Activity

> Describe any traffic determined to be suspicious and explain the evidence supporting that conclusion.

## 8. Indicators of Compromise

Document confirmed indicators such as:

* IP addresses
* Domains
* URLs
* Ports
* Hostnames
* File hashes
* User-Agent strings

## 9. Evidence

Screenshots supporting the investigation will be stored in:

```text
screenshots/
```

## 10. Conclusion

> Provide the final assessment of the network activity after completing the investigation.

## 11. Recommendations

> Add recommended defensive actions based on the investigation findings.

Examples may include:

* Blocking confirmed malicious IP addresses/domains
* Investigating affected endpoints
* Reviewing related authentication logs
* Monitoring for repeated network connections
* Performing additional endpoint investigation
