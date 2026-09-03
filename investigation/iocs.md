# Network Forensics — Indicators of Compromise

## Network Indicators

### IP Addresses

- `192.168.56.200`
  - Simulated server associated with suspicious HTTP activity.

### Hostnames

- `update-server.local`
  - Host associated with suspicious download and check-in traffic.

### HTTP Paths

- `/download/update.exe`
- `/api/checkin`

### Ports

- TCP/80
- TCP/8080

## Victim

`192.168.56.105`

## DNS

`example.com`

Note: `example.com` represents normal DNS activity in this controlled lab and is not considered a malicious IOC.
