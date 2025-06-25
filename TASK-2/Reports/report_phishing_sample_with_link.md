# Sample 2: `phishing_sample_with_link.txt` (Fake PayPal)

## 1.Sender's Email Address (Spoofing Check)
- **From:** `service@paypal.com`
- **Reply-To:** `paypal-alerts-center@consultant.com`
- **Observation:** 
  - `From` appears legitimate.
  - `Reply-To` is a non-affiliated domain (`consultant.com`).

---

## 2. Email Headers for Discrepancies
- **Received From:** `mail.fake-notification.com (203.0.113.55)`
- **Observation:** Sending domain and IP unrelated to PayPal infrastructure.

---

## 3. Suspicious Links or Attachments
- **Link:** `http://paypal.login-security-alerts.com/verify`
- **Observation:** Spoofed domain impersonating PayPal.
  - Real domain should be `https://www.paypal.com/signin`.
  - Lacks encryption since the site is http.

---

## 4. Urgent or Threatening Language
- “Failure to confirm your identity within 24 hours will result in permanent suspension.”
- Common scare tactic to prompt fast action.

---

## 5. Mismatched URLs
- **Displayed Link:** “Click here to verify your account”
- **Actual URL:** `paypal.login-security-alerts.com`
- **Observation:** Domain Impersonation with a spoofed webpage.

---

### 7. ✍️ Spelling / Grammar Errors
- No major spelling or grammatical errors.

---
