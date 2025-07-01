# John the Ripper

## Overview

**John the Ripper (JtR)** is a powerful and flexible open-source password cracking tool used by cybersecurity professionals, ethical hackers, and penetration testers. It is designed to identify weak passwords by attempting to "crack" their hash representations using dictionary attacks, brute-force, and custom rule-based transformations.

Originally developed for Unix-based systems, John now supports a wide variety of hash formats including MD5, SHA variants, bcrypt, and more. It is one of the most widely used tools in password security auditing.

---

## Usage in Password Strength Monitoring

John the Ripper plays a key role in evaluating the strength of password choices within a system. Its typical usage in password strength monitoring includes:

- Detecting **weak or guessable passwords**
- Simulating **real-world attacker behavior**
- Testing the **resilience of hashed credentials**
- Evaluating the **effectiveness of user education** and password policies

Security teams often use JtR to **test password policies** by attempting to crack user passwords using common or leaked wordlists, helping to flag risky accounts before attackers can exploit them.

---

## Password Strength Analysis Using JtR

In this project, I used **John the Ripper** to test the strength of custom-created Indian-style passwords. The process involved the following steps:

### 1. Generating Wordlists
We created three types of password lists:
- **Simple passwords** (e.g., `arun2002`, `neha123`)
- **Medium strength** (e.g., `sumit@1443`, `tanyaDance2023`)
- **Complex passwords** (e.g., `G0kul_LuvsK@adal143!`, `HorseBatteryStaple`)

### 2. Hashing the Passwords
These plaintext passwords were hashed using various algorithms like **MD5**, **SHA1**, **SHA26**, and **SHA-512** to simulate real-world storage formats. We ensured the hash file contained only the hash values to match JtR input requirements.

### 3. Creating a Custom Wordlist
I merged the weak, medium, and a few complex passwords with common entries from `rockyou.txt` to build a smart, targeted 200-entry wordlist (`vyshnav-wordlist.txt`).

### 4. Cracking the Hashes
I used JtR with the proper hash format to crack the password hashes:
```
john --format=hash-type --wordlist=wordlist.txt hashes.txt
```
