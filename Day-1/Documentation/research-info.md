# Network Reconnaissance
- Network reconnaissance is the process of gathering information about a target network to understand its structure, active devices, open ports, and running services. It's a crucial first step in both ethical hacking and cybersecurity assessments.
- Mainly there are 2 types of reconnaissance :
 - Passive reconnaissance : Observing the network without directly interacting with it (e.g., sniffing traffic).
 - Active reconnaissance : Actively sending packets to discover devices and services (e.g., using tools like Nmap).

## Tools used to carry out reconnaissance 
### Active Reconnaissance
- Nmap : Nmap (Network Mapper) is an open-source network scanning tool created by Gordon Lyon (also known by the pseudonym Fyodor). It was first released in 1997 and is used in Host discovery,port scanning, service & OS detection and network mapping.
- Masscan : Masscan is an ultra-fast network port scanner created by Robert David Graham. It's designed specifically for speed, capable of scanning the entire IPv4 internet in a matter of minutes under ideal conditions.

### Passive Reconnaissance
- Wireshark: Wireshark is a free and open-source packet analyzer created by Gerald Combs in 1998. It is used for capturing and inspecting live network traffic, analyzing protocols, identifying communication between hosts, and detecting sensitive data or anomalies in network behavior.
- tcpdump: tcpdump is a command-line packet sniffer developed by Van Jacobson, Craig Leres, and Steven McCanne. It captures and filters raw network traffic using the libpcap library and is used in live traffic monitoring, diagnostics, packet analysis, and saving captures for further inspection.
- Shodan: Shodan is an internet-facing device search engine created by John Matherly in 2009. It passively indexes publicly accessible devices and services and is used in external reconnaissance, identifying exposed systems, collecting service banners, and mapping internet-facing infrastructure.

## Concepts
### *Ports*
- Ports are logical endpoints for network communication, identified by port numbers (0–65535). They allow multiple services to run on a single IP address.
 - 0–1023: Well-known ports (e.g., 22 for SSH, 80 for HTTP, 443 for HTTPS)
 - 1024–49151: Registered ports (used by software vendors)
 - 49152–65535: Dynamic/private ports (used for temporary client connections)
> [[source]](https://en.wikipedia.org/wiki/Port_(computer_networking))

### TCP/IP
- TCP/IP (Transmission Control Protocol/Internet Protocol) is the foundational networking protocol suite used for communication over the internet and most local networks.
- Core layers :
 1. Application Layer – Handles data exchange (e.g., HTTP, FTP, DNS).
 2. Transport Layer – Manages end-to-end communication:
  1. TCP (reliable, connection-oriented)
  2. UDP (faster, connectionless)
 3. Internet Layer – Handles addressing and routing (e.g., IP, ICMP).
 4. Link Layer – Deals with physical hardware and MAC addressing (e.g., Ethernet, Wi-Fi).
- TCP/IP enables packet-based communication, where data is broken into packets, routed independently, and reassembled at the destination.
> [[source]](https://en.wikipedia.org/wiki/Port_(computer_networking))
 ### 7 Layer OSI Model
 - The OSI (Open Systems Interconnection) model standardizes network communication into 7 layers, from physical transmission to application-level interactions.
 - Layers(From Top to bottom):
   - Application (Layer 7) – User interaction (e.g., HTTP, SMTP, FTP)
   - Presentation (Layer 6) – Data formatting, encryption/decryption (e.g., SSL/TLS, JPEG)
   - Session (Layer 5) – Connection management (e.g., session initiation, teardown)
   - Transport (Layer 4) – End-to-end delivery, error handling (e.g., TCP, UDP)
   - Network (Layer 3) – Routing and addressing (e.g., IP, ICMP)
   - Data Link (Layer 2) – MAC addressing, frame handling (e.g., Ethernet, ARP)
   - Physical (Layer 1) – Transmission of raw bits over media (e.g., cables, radio signals)
 - Layers(1-4) are transport layers,Layers(5-7) are Apllication Layers
> [[source]](https://www.geeksforgeeks.org/open-systems-interconnection-model-osi/)

 ### CIDR Notation
 - CIDR stands for Classless Inter-Domain Routing. It represents IP addresses along with their subnet mask using a slash `/` format.
 - `/24` represents 256 addresses, and this defines the subnet clearly as `255.255.255.0`
 - Essential for routing and firewall rules, network planning, and recon tools like Nmap
