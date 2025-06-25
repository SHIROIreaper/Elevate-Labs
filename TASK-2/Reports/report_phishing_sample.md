# Phishing Email Static Analysis Report

---

## Sample 1: `phishing_sample.txt` (Inheritance Scam)

### 1. Sender's Email Address (Spoofing Check)
- **From:** `vieria@aol.com`
- **Reply-To:** `carrr444@yahoo.com`
- **Observation:** 
  - Suspicious use of free email services.
  - Mismatch between `From` and `Reply-To`.
  - No official or organizational domain.

---

### 2. Email Headers for Discrepancies
- **SPF Result:** Neutral
- **Sender IP:** `85.250.54.29` (Israel) – unrelated to claimed origin (Guinea-Bissau)
- **Received Chains:** Routed through Taiwan and `bigfish.com` servers
- **Observation:** Header paths and sender IP are suspicious and unrelated to sender’s claimed identity.

---

### 3. Suspicious Links or Attachments
- **Observation:** None attached.

---

### 4. Urgent or Threatening Language
- “Help me receive this money… you will get 30%.”

---

### 5. Mismatched URLs
- **Result:** None present in this message.
---

### 8. ✅ Summary of Traits

---
