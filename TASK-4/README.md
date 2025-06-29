# Setup and Use a Firewall on Windows/Linux
## Objective

Configure and test basic firewall rules to allow or block traffic.
---

## Tools Required

- [**Linux Terminal**](./Documentation//Firewall_and_UFW.md) – For managing UFW and Netcat.
- [**Netcat (`nc`)**](./Documentation/connection_establish.md) – To establish and test raw TCP communication.
- [**UFW (Uncomplicated Firewall)**](./Documentation//Firewall_and_UFW.md) – To apply firewall rules simply.
- [**Wireshark**](https://github.com/SHIROIreaper/Elevate-Labs/blob/main/Day-1/Documentation/Wireshark.md) – For optional traffic capture and analysis.
- [**Android with Termux**](https://f-droid.org/en/packages/com.termux/) – To test cross-device connection from a phone.

---

## Result

- ✅ [Established a communication channel between devices](./docs/establish_connection.md) using port 23 (Telnet-style).
- ✅ [Configured firewall rules](./docs/firewall_ufw_guide.md#3-basic-ufw-commands) to allow/block specific ports.
- ✅ Verified blocked traffic results in **silent failure** (no “connection denied” message), consistent with packet dropping behavior.
- ✅ [Gained hands-on experience](./docs/firewall_ufw_guide.md#5-example-blocking-telnet-communication) with port-level control and basic networking tools.

---

