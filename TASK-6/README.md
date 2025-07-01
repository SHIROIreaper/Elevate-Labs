# Password Strength Analysis using John the Ripper

## Overview

This project focuses on evaluating the strength of various password types—ranging from simple to complex—by simulating real-world cracking scenarios. By generating custom wordlists and comparing them against hashed password files, the project highlights how password complexity influences resistance to common attacks.

The study emphasizes how easily weak passwords can be compromised using modern cracking tools and serves as a foundational exploration into password auditing techniques used in cybersecurity.

---

## Objective

Understand what makes a password strong and test it against password strength tools.

---

## Tools Used in cracking **password hashes**

To conduct password strength analysis and perform cracking operations, the following tools are commonly used:

- **John the Ripper (JtR)**: A fast, flexible password cracking tool supporting multiple hash formats.
- **Hashcat**: A GPU-accelerated password recovery tool capable of high-performance brute-force and dictionary attacks.
- **Hydra**: Network login cracker for attacking services over protocols such as SSH, FTP, etc. (less relevant for offline hash cracking)
- **Hash Generators**: For converting plaintext passwords into hash formats (e.g., `md5sum`, `openssl`, Python scripts)

- For this analysis, [**John the Ripper**](./Documentation/JohnTheRipper.md) was selected due to its support for custom wordlists, ease of use, and compatibility with various hash formats including MD5 and SHA variants.

>  Hash generation was performed using command-line utilities (`md5sum`) and shell scripts, and the resulting hashes were passed to John for cracking against curated wordlists.

---

## Results / Findings

- Various passwords were analysed and the results showed:
 - [**Simple passwords**](./Wordlists/plaintext/plaintext-simple.txt) were cracked almost instantly using dictionary attacks.
 - [**Medium-strength passwords**](./Wordlists/plaintext/plaintext-medium.txt) showed moderate resistance, but many still succumbed when variations (symbol substitutions, dates) were included in the wordlist.
 - [**Complex passwords**](./Wordlists/plaintext/plaintext-complex.txt), particularly those using regional and emotional entropy, resisted cracking attempts, highlighting the value of unpredictable character combinations.
 - The test demonstrated how attackers could exploit weak password patterns using public or slightly modified dictionaries.

The project underscores the need for robust password creation habits and proactive auditing practices using available open-source tools.

