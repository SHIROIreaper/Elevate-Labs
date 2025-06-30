# Wireshark Packet Analysis - Network Traffic Capture

## Overview
This project focuses on performing live packet capture using Wireshark on an active network interface. The goal is to observe real-time network traffic, identify various protocols in use, and understand basic packet-level communication through filtering and export.

For organized review and replication, all outputs and summaries are maintained in dedicated directories.

Refer to the [overview/](./overview/) for supporting context.

---

## Objective

Capture live network packets and identify basic protocols and traffic types

---

## Tools Required

The following tools and configurations were used throughout the project:
- [**Wireshark**:](https://github.com/SHIROIreaper/Elevate-Labs/blob/main/Day-1/Documentation/Wireshark.md) Packet capture and inspection.
- **Ping / Web Browser**: To generate traffic.

Full environment setup steps and command references are stored in [tools/setup.md](./tools/setup.md).

---

## Results
The packet capture has been completed and exported. Analysis focused on common protocols such as:
- **HTTP**
- **DNS**
- **TCP**
- **ICMP**

Key findings, filters used, and observed traffic patterns are documented in:
- [results/summary.md](./results/summary.md)
- [results/wireshark-traffic.pcap](./results/wireshark-traffic.pcap)

This directory also contains insights into protocol behaviors and timestamps aligned with test activities.

---

**Note**: All directories contain raw data, analysis notes, or logs relevant to the corresponding step.

