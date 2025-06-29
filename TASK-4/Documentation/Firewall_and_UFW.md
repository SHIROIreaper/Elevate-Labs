# Firewall and UFW Documentation Guide

## Objective

To understand the role of firewalls in system and network security, with a focus on using UFW (Uncomplicated Firewall) for rule management, traffic control, and practical examples.

---

## 1. What is a Firewall?

A **firewall** is a network security system that monitors and controls incoming and outgoing traffic based on predefined security rules. It acts as a barrier between trusted and untrusted networks.

### Types of Firewalls:
- **Host-based Firewall**: Installed on a single device (e.g., UFW on Linux).
- **Network-based Firewall**: Positioned at the network perimeter (e.g., hardware appliances or enterprise solutions).

---

## 2. UFW (Uncomplicated Firewall)

UFW is a frontend for `iptables`, designed to make managing firewall rules easier on Debian-based systems (like Ubuntu and Kali Linux).

### Key Features:
- Simple command-line syntax
- Default deny incoming policy
- Supports logging, app profiles, and IPv6

---

## 3. Basic UFW Commands

### Enable/Disable UFW
```
sudo ufw enable
sudo ufw disable
```

### Check Status
```
sudo ufw status
sudo ufw status verbose
```
### Set Default Policies
```
sudo ufw default deny incoming
sudo ufw default allow outgoing
```
### Allow Specific Ports
```
sudo ufw allow 22       # Allow SSH
sudo ufw allow 80/tcp   # Allow HTTP
```
### Deny Specific Ports
```
sudo ufw deny 23/tcp    # Deny Telnet
```
### Delete Rules
```
sudo ufw delete allow 80/tcp
```
