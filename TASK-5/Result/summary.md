# Summary

# Summary of Wireshark Protocol Capture and Analysis

## Packet Capture Context

The traffic was captured during a basic web browsing session using Firefox. The browser was directed to `https://proxiyum.com`, and the capture was filtered and exported into four protocol-specific files:

- `dns.pcapng`
- `tcp.pcapng`
- `udp.pcapng`
- `http.pcapng`

The goal was to understand how various network protocols function in the background of a standard HTTPS web session.

---

## Protocol Flow and Observations

### DNS (Domain Name System)

Captured in: `dns.pcapng`  
Transport: UDP

- Firefox initiated a DNS query for `proxiyum.com`.
- The client sent a query over UDP (port 53) to a DNS resolver.
- The response included an A record mapping the domain to an IPv4 address.
- This step was required before the browser could establish a TCP connection.

**DNS is a prerequisite** in domain-based communication and typically uses UDP for fast, connectionless queries.

---

### TCP (Transmission Control Protocol)

Captured in: `tcp.pcapng`

- A standard 3-way handshake was observed:
  - `SYN` from the client
  - `SYN-ACK` from the server
  - `ACK` from the client
- This handshake established a reliable session before any encrypted data was transmitted.
- TCP ensured ordered, lossless delivery and session maintenance.

**TCP is the foundation** for reliable delivery, and required for encrypted HTTPS traffic.

---

### UDP (User Datagram Protocol)

Captured in: `udp.pcapng`

- Primarily used for the DNS traffic, which does not require session setup or guaranteed delivery.
- The packets were small, efficient, and consisted of only one request and one response per domain resolution.

**UDP is preferred** for fast, one-off communication like DNS, VoIP, and streaming.

---

### HTTP (Hypertext Transfer Protocol)

Captured in: `http.pcapng`  
Transport: TCP (port 443, HTTPS)

- Very few or no readable HTTP packets were observed due to encryption via TLS.
- TLS encapsulates HTTP traffic, making it unreadable unless decrypted.
- SNI (Server Name Indication) in the TLS handshake may have revealed the domain `proxiyum.com`, but not the request/response content.

**In HTTPS sessions**, HTTP data exists but is encrypted by TLS. Only metadata (e.g., domain names) may be visible.

---

## Insights and Conclusions

- Visiting a website, even without logging in, involves multiple protocols working in sequence.
- **DNS → TCP → TLS → HTTP** forms the layered stack during an HTTPS session.
- DNS and TCP metadata are clearly visible and useful for analysis.
- HTTPS protects the content, but protocol behavior (handshakes, queries, ports) remains visible.
- Wireshark allows full inspection of these layers and is critical for learning and diagnostics.

This analysis confirms that even basic browsing reveals protocol interactions critical to understanding real-world networking and security fundamentals.
