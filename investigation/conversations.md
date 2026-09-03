# Network Conversation Analysis

## Objective

Analyze network conversations to identify significant communication between hosts.

## Conversations

| Source | Source Port | Destination | Destination Port | Protocol | Notes |
| ------ | ----------: | ----------- | ---------------: | -------- | ----- |
| TBD    |         TBD | TBD         |              TBD | TBD      | TBD   |
| TBD    |         TBD | TBD         |              TBD | TBD      | TBD   |

## Wireshark Analysis

The investigation will use:

**Statistics → Conversations**

The following will be reviewed:

* IPv4 conversations
* IPv6 conversations
* TCP conversations
* UDP conversations
* Packet counts
* Byte counts
* Duration
* Source and destination addresses
* Source and destination ports

## Suspicious Connections

Potentially suspicious connections will be investigated based on:

* Unusual destination IP addresses
* Unexpected ports
* Repeated connections
* Large data transfers
* Long-duration sessions
* Unusual communication patterns

## Stream Analysis

Where appropriate, network streams will be reconstructed using Wireshark's:

**Follow → TCP Stream**

or

**Follow → UDP Stream**

## Findings

> Findings will be added after analysis of the PCAP.

## Conclusion

Conversation analysis will help establish which hosts communicated, how they communicated, and which connections require deeper investigation.
