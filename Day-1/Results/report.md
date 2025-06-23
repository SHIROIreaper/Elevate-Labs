# Network Reconnaissance Report

## 1. Objective

Learn to discover open ports on devices in your local network to understand network exposure.

---

## 2. Recon Performed

Used Nmap to scan the local `/24` subnet and identify live hosts, open ports, and service versions.

### Nmap Commands Used:
- `-p-` : Full TCP port range scan (1-65535)
- `-sS` : TCP SYN scan
- `-sV` : Service/version detection
- `--script vuln` : Run built-in vulnerability detection scripts
- `-T4` : Aggressive scan timing
- `-F` : Fast scan of top 100 ports
- `-sn -PE` : ICMP Echo ping scan (did not work)
- `-sn -PP -PM` : ICMP Timestamp and Address Mask (worked)

### Observations:
- Full port scan (`-p-`) identified services running on non-standard ports missed by default scans.
- `--script vuln` revealed outdated or misconfigured services on HTTP and SMB.
- TCP SYN scans `-sS` helped avoid triggering some basic IDS (Intrusion Detection System).

---

## 3. ICMP Discovery Issue

Initial host discovery using:
`nmap -sn -PE 192.168.1.0/24`

Returned no responses. Likely due to Echo Requests (Type 8) being blocked by firewall.
`nmap -sn -PP -PM 192.168.1.0/24`
These probes (ICMP Timestamp and Address Mask) returned responses and helped identify live hosts.

## 4. Wireshark Analysis
To tackle the icmp discovery problem, used wireshark and filtered for icmp and understood the types and functions of different protocols.
### Observations:
- Understood the network traffic and how router communicate with the devices inside the network.
- Grasped the concepts of CIDR notation, TCP/IP, OSI structure, and protocols.
> Using the knowledge of python and nmap, created a custom python script which automates the nmap scans.[[Github Link]](https://github.com/SHIROIreaper/nmap-automation)

