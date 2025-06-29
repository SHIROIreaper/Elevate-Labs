
# Vulnerability Scanning with Nessus

## Overview  
This document outlines the process of setting up **Nessus Essentials** and performing a vulnerability scan on a local machine. The goal is to identify potential vulnerabilities and gain hands-on experience with a widely-used vulnerability scanning tool.

## Objective  
1. Install Nessus Essentials  
2. Set up scan target (local machine IP or `localhost`)  
3. Start a full vulnerability scan  
4. Wait for scan to complete (approx. 30–60 mins)  
5. Review the report for vulnerabilities and severity  
6. Research basic fixes or mitigations  
7. Document the most critical vulnerabilities  
8. Take screenshots of the scan results  

## Tools Used  

- **[Nessus Essentials](https://www.tenable.com/products/nessus/nessus-essentials)** – A free vulnerability scanner by Tenable  
  > Refer to the [official installation documentation](https://docs.tenable.com/nessus/Content/InstallNessus.htm) for setup instructions.

## Results  

Nessus Essentials was successfully installed and a local scan was executed. Key learnings include:

- Initiating a full system vulnerability scan  
- Interpreting results by severity levels (low, medium, high, critical)  
- Understanding common misconfigurations and known CVEs  
- Exploring possible remediations or workarounds  

Refer to the following subdirectories for evidence and references:  
- 📂 [Scan Configuration & Execution](./screenshost/config/)  
- 📂 [Generated Report screenshots](./screenshots/vuln/)  
- 📂 [Critical Findings & Notes](./Reports/)

This exercise emphasized the value of periodic scanning, patch management, and baseline hardening for local systems.

## Related Resources  

- [Nessus Setup Guide](https://docs.tenable.com/nessus/Content/InstallNessus.htm)  
- [Nessus Essentials Product Page](https://www.tenable.com/products/nessus/nessus-essentials)  
- [Example Nessus Report Screenshot](https://assets.tenable.com/prod-images/Nessus/Nessus-Vulnerability-Report.png)
