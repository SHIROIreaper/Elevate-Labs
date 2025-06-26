# Vulnerability Scanning with Nessus

## Overview  
This document outlines the process of setting up Nessus Essentials and performing a vulnerability scan on a local machine. The goal is to identify potential vulnerabilities and gain familiarity with the usage of basic vulnerability scanning tools.

## Objective  
1.  Install OpenVAS or Nessus Essentials.
2. Set up scan target as your local machine IP or localhost.
3. Start a full vulnerability scan.
4. Wait for scan to complete (may take 30-60 mins).
5. Review the report for vulnerabilities and severity.
6. Research simple fixes or mitigations for found vulnerabilities.
7. Document the most critical vulnerabilities.
8. Take screenshots of the scan results.

## Tools Used  

- **Nessus Essentials**  
  A free version of the Nessus vulnerability scanner by Tenable, useful for educational and small-scale security assessments.  

  ### Basic Installation Guide  
  1. Download Nessus Essentials from the [official Tenable website](https://www.tenable.com/products/nessus/nessus-essentials)  
  2. Install it using the package manager for your OS (e.g., `dpkg -i` on Debian-based systems)  
  3. Start the Nessus service:  
     ```bash
     sudo systemctl start nessusd
     ```  
  4. Access the Nessus web interface:  
     ```
     https://localhost:8834
     ```  
  5. Register using the activation code sent to your email  
  6. Wait for plugin updates to complete  
  7. Begin using the scanner

## Results  

I successfully installed Nessus Essentials and configured a basic scan targeting the local host. During the scan process, learned :

- How to initiate a full vulnerability scan  
- How to review results for different severity levels (low, medium, high, critical)  
- Gained awareness about common vulnerabilities and ways to mitigate them  

This activity helped reinforce the importance of regular scanning, proper service configuration, and software updates to maintain system security.

## Related Resources  

- [Nessus Setup Guide](https://docs.tenable.com/nessus/Content/InstallNessus.htm)  
- [Sample Nessus Report](https://www.tenable.com/products/nessus-vulnerability-scanner)  
- [Screenshot Sample (Local Scan)](https://assets.tenable.com/prod-images/Nessus/Nessus-Vulnerability-Report.png)
