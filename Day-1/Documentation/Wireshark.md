# Wireshark

## Overview
Wireshark is a free, open-source packet analyzer used for network traffic inspection, protocol analysis, and troubleshooting. It supports real-time and offline capture of packets across various protocols.

## Key Features
- Deep inspection of hundreds of protocols
- Live capture and offline analysis
- Filtering support (capture/display)
- Packet color coding and TCP stream reassembly
- Supports pcap and pcapng formats

## Common Use Cases
- Network troubleshooting
- Security analysis
- Reverse engineering of protocols
- Monitoring application-layer traffic
- Packet-level inspection for incident response

## Capture Filters (BPF Syntax)
Applied **before** capture begins:
- `tcp port 80` — capture only HTTP traffic
- `icmp` — capture ICMP packets only
- `host 192.168.1.1` — capture traffic to/from host

## Display Filters (Wireshark Syntax)
Used to analyze captured packets:
- `ip.addr == 192.168.1.1`
- `tcp.flags.syn == 1`
- `icmp.type == 8`
- `http.request.method == "GET"`

## Performance Notes
- Capturing on high-throughput interfaces requires hardware support (e.g., promiscuous mode, ring buffer tuning)
- Large captures impact RAM/CPU; use filters to minimize load

## Security Considerations
- Can expose sensitive data in plaintext protocols
- Requires elevated privileges for live capture
- Do not capture on production systems without authorization

## Alternatives
- tcpdump (CLI-based)
- TShark (Wireshark CLI)
- NetworkMiner (passive analysis)
