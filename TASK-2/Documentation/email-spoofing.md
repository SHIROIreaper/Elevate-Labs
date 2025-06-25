# Overview

This document contains the concepts on **email spoofing** and related topics.
---

## 1. What is Email Spoofing?

A technique in which attackers falsify metadata—like the `From`, `Reply-To`, or `Return-Path` header fields—to impersonate a legitimate sender.  

---

## 2. Types of Email Spoofing

- **Display Name Spoofing**: The visible name (e.g., “Your Bank”) is faked while the actual email address is malicious.  
- **Domain Spoofing**: Attackers use look-alike domains (e.g., `paypaI.com`) or fake domains to deceive users.  
- **Header Spoofing**: Forging header fields during SMTP transfer to misdirect replies or bounces.  
- **Look-alike / Unicode (Homograph) Attacks**: Using confusing characters (e.g., Cyrillic “а” vs Latin “a”) to mimic domains.  
- **Internal Spoofing / BEC**: Impersonating internal colleagues or executives to authorize payments or data transfers.  
  [[source]](https://www.proofpoint.com/us/blog/email-and-cloud-threats/preventing-vendor-compromise-attacks)

---

## 3. What Can Be Achieved Through Spoofing?

| Goal                     | Outcome Description |
|--------------------------|---------------------|
| **Phishing / Credential Theft** | Victims are directed to fake login pages to steal passwords. |
| **Malware Delivery**     | Attachments or URLs deliver ransomware, Trojans, or spyware. |
| **Financial Fraud / BEC**| Employees are tricked into wiring funds to attacker-controlled accounts. |
| **Account Takeover**     | Password-reset emails are redirected to attacker inboxes. |
| **Reputation Damage**    | Brand trust is damaged through impersonated messages. |
| **Internal Data Breach** | Targeted spear-phishing leads to sensitive data exfiltration. |

[[source]](https://www.proofpoint.com/us/threat-reference/domain-spoofing)

---

## 4. Why Spoofing Remains Effective

- The SMTP protocol has **no built‑in authentication**, so headers can easily be forged.  
- Many domains still lack **SPF**, **DKIM**, and/or **DMARC** protection.  
- Recipients often **trust display names** and don’t verify full email addresses.  
[[Roots of SMTP spoofing]](https://www.wired.com/2012/01/google-microsoft-yahoo-paypal-go-after-phishers-with-new-email-authentication-effort)

---

## 5. Prevention (Essential Steps)

1. **Implement SPF, DKIM & DMARC** policies to authenticate legitimate senders.  
   [Complete guide to email authentication](https://dmarcly.com/blog/how-to-implement-dmarc-dkim-spf-to-stop-email-spoofing-phishing-the-definitive-guide)  
2. **Verify the true sender address**, not just the display name.  
3. **Monitor and block homograph/look‑alike domains** proactively.  
4. **Deploy filtering and anomaly detection tools** to flag unusual emails.  
5. **Raise user awareness** about social engineering and header inspection.  
[[source]](https://www.proofpoint.com/us/blog/email-and-cloud-threats/prevent-email-spoofing-with-dmarc)

---


