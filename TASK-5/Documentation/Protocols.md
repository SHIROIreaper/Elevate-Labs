# Common Network Protocols by OSI Layer

---

## Application Layer (Layer 7)

### HTTP (HyperText Transfer Protocol)
Used for web communication and content delivery.  
Port: 80/TCP

### HTTPS (HTTP Secure)
Encrypted version of HTTP using TLS/SSL.  
Port: 443/TCP

### DNS (Domain Name System)
Resolves domain names to IP addresses.  
Port: 53/UDP and 53/TCP

### FTP (File Transfer Protocol)
Transfers files between client and server.  
Ports: 21/TCP (control), 20/TCP (data)

### SSH (Secure Shell)
Provides secure remote access and command-line interface.  
Port: 22/TCP

### Telnet
Unsecured remote terminal access.  
Port: 23/TCP

### SMTP (Simple Mail Transfer Protocol)
Sends emails between servers.  
Port: 25/TCP

### POP3 (Post Office Protocol v3)
Retrieves emails from server to client.  
Port: 110/TCP

### IMAP (Internet Message Access Protocol)
Accesses and manages email on a mail server.  
Port: 143/TCP

### SNMP (Simple Network Management Protocol)
Monitors and manages network devices.  
Port: 161/UDP

### NTP (Network Time Protocol)
Synchronizes clocks between systems.  
Port: 123/UDP

### LDAP (Lightweight Directory Access Protocol)
Accesses and maintains directory services.  
Port: 389/TCP

### RDP (Remote Desktop Protocol)
Provides GUI-based remote desktop access.  
Port: 3389/TCP

### SIP (Session Initiation Protocol)
Establishes and manages VoIP calls.  
Port: 5060/UDP or TCP

### SMB (Server Message Block)
Shares files and printers in Windows networks.  
Ports: 445/TCP, 139/TCP

---

## Transport Layer (Layer 4)

### TCP (Transmission Control Protocol)
Reliable, connection-oriented protocol for data transmission.  
Ports: Varies (used by HTTP, HTTPS, FTP, etc.)

### UDP (User Datagram Protocol)
Connectionless protocol for fast, real-time communication.  
Ports: Varies (used by DNS, NTP, etc.)

---

## Network Layer (Layer 3)

### ICMP (Internet Control Message Protocol)
Used for network diagnostics like `ping` and `traceroute`.  
No port (not port-based)

---

## Data Link Layer (Layer 2)

### ARP (Address Resolution Protocol)
Maps IP addresses to MAC addresses on a local network.  
No port (operates directly over Layer 2)

