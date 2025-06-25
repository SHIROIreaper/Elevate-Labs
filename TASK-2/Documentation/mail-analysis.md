# Email Analysis

This document provides a practical understanding of email analysis, header analysis, and related topics.

---

## Common Goals of a email spoofing :
- Trick recipients into opening malicious links or attachments
- Bypass spam filters or impersonate authority
- Launch phishing or Business Email Compromise (BEC) attacks

---

## 1. Anatomy of an Email Header

An email header contains metadata that traces the email’s journey from sender to recipient. Key fields to inspect:

| Field          | Purpose                                                  |
|----------------|----------------------------------------------------------|
| `From`         | Name and address shown to recipient (can be spoofed)     |
| `Reply-To`     | Where replies go (can differ from `From`)                |
| `Return-Path`  | Bounces/errors return here — often reveals real sender   |
| `Received`     | Shows hops between mail servers (read bottom-up)         |
| `Message-ID`   | Unique ID, usually created by sender’s email server      |
| `DKIM`, `SPF`, `DMARC` | Email authentication checks                       |

---

## 2. Spotting a Spoofed Email

Here’s how you can identify a spoofed or suspicious email:

- **Mismatch** between display name and actual email domain
- **Header inconsistencies** in `Received` chain or `Return-Path`
- **No DKIM/SPF/DMARC alignment** or failing status
- **Urgent or emotional language** prompting action
- **Suspicious URLs** (hover to verify destination)
- **Generic greetings** or grammar issues

---

## 3. Authentication Protocols

| Protocol | Role                                      |
|---------|-------------------------------------------|
| SPF     | Lists authorized IPs for sending domain   |
| DKIM    | Signs the email to verify content         |
| DMARC   | Policy framework for SPF/DKIM handling    |

All three work to validate sender identity.

---

## 4. Tools for Analysis

- `Whois` & `nslookup` — for domain tracing
- Online email header analyzers
- Browser dev tools — inspect link destinations
- Threat intel platforms (e.g. VirusTotal, AbuseIPDB)

---

