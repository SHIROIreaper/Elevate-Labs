
# Nessus

## Purpose  
Nessus is a widely used vulnerability assessment tool developed by Tenable. Its primary purpose is to identify security vulnerabilities in systems, applications, and network infrastructure. It is extensively used by cybersecurity professionals to:

- Discover open ports and services  
- Detect software flaws and misconfigurations  
- Evaluate patch levels and compliance issues  
- Help in proactive risk management and remediation  

By scanning target machines, Nessus enables organizations to mitigate vulnerabilities before they can be exploited by attackers.

## Setup  

1. **Download Nessus Essentials** from the [official Tenable website](https://www.tenable.com/products/nessus/nessus-essentials)  
2. **Install the package** using your OS's package manager. For Debian-based systems:  
   ```bash
   sudo dpkg -i Nessus-*.deb
   sudo apt-get install -f
   ```  
3. **Start the Nessus service**:  
   ```bash
   sudo systemctl start nessusd
   ```  
4. **Access the Web Interface**:  
   Open your browser and go to:  
   ```
   https://localhost:8834
   ```  
5. **Register Nessus** with the activation code emailed to you  
6. **Wait for plugins to compile and update** (this may take several minutes)  
7. **Login and create a scan** from the dashboard interface

## Type of Scan  
Nessus supports a variety of scan types tailored to different environments and needs:

- **Basic Network Scan**: Detects open ports and common vulnerabilities  
- **Advanced Scan**: Customizable scans with fine-grained control over plugins, ports, and credentials  
- **Credentialed Scan**: Allows deeper inspection by authenticating into systems to assess internal configurations  
- **Web Application Scan**: Targets web services for vulnerabilities like XSS, SQL injection, etc.  
- **Compliance Scan**: Checks against security benchmarks (CIS, DISA, etc.)

For this setup, a **Basic Network Scan** was performed targeting the local machine to identify surface-level vulnerabilities and assess exposed services.

## Analyse Scan Report  
The generated scan report provides a detailed breakdown of identified issues:

- **Severity Levels**: Each finding is categorized as *Informational*, *Low*, *Medium*, *High*, or *Critical*, helping prioritize remediation  
- **Affected Services**: Reports show which ports and protocols are vulnerable  
- **Vulnerability Description**: Explains the issue, potential impact, and technical background  
- **Recommended Fixes**: Provides guidance on patching, configuration changes, or mitigation steps

Reviewing the report enhances the analyst’s ability to distinguish between false positives, exploitable issues, and configuration weaknesses.

## Professional Use  
In professional environments, Nessus is commonly integrated into routine security practices:

- **Vulnerability Management Programs**  
- **Internal Audits and Risk Assessments**  
- **Regulatory Compliance Verification (e.g., PCI-DSS, HIPAA)**  
- **Patch Management Validation**  
- **Penetration Testing Preparation**

Security analysts, system administrators, and auditors use Nessus to maintain system hygiene, track remediation efforts, and verify security posture improvements over time.

Regular and scheduled scans, combined with actionable reporting, make Nessus a cornerstone tool in a cybersecurity professional’s toolkit.
