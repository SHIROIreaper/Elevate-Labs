# Establishing Connection Between Devices Using Netcat

## Objective

To establish a basic TCP connection between two devices over a specified port (e.g., port 23) using **Netcat** (nc). This document covers Netcat basics, prerequisites, and step-by-step procedures to achieve successful communication.

---

## What is Netcat?

**Netcat (nc)** is a command-line utility used for:
- Reading and writing data across network connections
- Debugging and network exploration
- Setting up TCP/UDP client-server communication

Netcat does not provide encryption, authentication, or sophisticated controls, but is invaluable for raw socket testing and port-based communication.

---

## Tools Required

- **Linux system** (with Netcat installed)
- **Android phone with Termux** (optional)
- Both devices must be on the same network or reachable over the internet
- Firewall (e.g., `ufw`) properly configured

---

## Steps to Establish Connection
Check whether netcat is already installed with ```nc -h```
### On Termux(Phone):
```
pkg update
pkg install netcat
```
### On PC(Linux):

#### For Debian:
```
sudo apt update
sudo apt install netcat-traditional
```
#### For Fedora/CentOS/RHEL:
```
sudo dnf install nc
```
#### For Arch Linux:
```
sudo pacman -S gnu-netcat
```
### On Windows:
- Download nmap suite first which include ncat.
- Refer [this link](https://nmap.org/ncat/) for more information.

###  Setup Listener on One Device (Server Side)
```
 nc -l -p 23
```
### Connect From the Second Device
```
 nc <IP-of-listener> 23

```

