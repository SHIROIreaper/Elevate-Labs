# Setup and Use a Firewall on Windows/Linux
## Objective

Configure and test basic firewall rules to allow or block traffic.
---

## Tools Required

- [**Netcat (`nc`)**](./Documentation/connection_establish.md) – To establish and test raw TCP communication.
- [**UFW (Uncomplicated Firewall)**](./Documentation//Firewall_and_UFW.md) – To apply firewall rules simply.
- [**Wireshark**](https://github.com/SHIROIreaper/Elevate-Labs/blob/main/Day-1/Documentation/Wireshark.md) – For optional traffic capture and analysis.
- [**Android with Termux**](https://f-droid.org/en/packages/com.termux/) – To test cross-device connection from a phone.

---

## Result

- ✅ [Established a communication channel between devices](./Screenshots/port_communication.png) using port 23 (Telnet) and then to port 22 (ssh).
- ✅ [Configured firewall rules](./Screenshots/rules_set.png) to allow/block specific ports.
- ✅ [Verified blocked traffic results](./Screenshots/attacker_side/) in **silent failure** (no “connection denied” message), consistent with packet dropping behavior.
- ✅ Gained hands-on experience with port-level control and basic networking tools.

---

