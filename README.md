# Phishing-Email-Analysis-Report

##  Objective
Identify phishing characteristics in a suspicious email.


##  Phishing Email Sample

**Subject:** Urgent: Your Account Will Be Suspended  
**From:** security@paypa1.com  

**Email Body:**
```
Dear Customer,

We have detected suspicious activity in your account. Please verify your identity by clicking the link below:

👉 [Verify Now](http://malicious-site.com/paypal-login)

Failure to verify your account within 24 hours will result in permanent suspension.

Regards,  
PayPal Security Team
```

##  Header Analysis (Simulated)

| Header Field         | Suspicious Detail                         |
|----------------------|-------------------------------------------|
| From:                | security@paypa1.com (spoofed domain)      |
| Reply-To:            | phish@fake-domain.ru                      |
| Return-Path:         | mailer@unknownsite.biz                    |
| Received:            | Source IP from an untrusted server        |
| SPF/DKIM/DMARC       | Failed all authentication checks          |

---

##  Phishing Indicators Identified

| # | Type                | Details |
|--:|---------------------|---------|
| 1 | Spoofed Email       | `paypa1.com` (looks like `paypal.com`) |
| 2 | Threat Language     | "Your account will be suspended..."    |
| 3 | Urgency             | "within 24 hours"                      |
| 4 | Suspicious Link     | Fake URL: `http://malicious-site.com` |
| 5 | Header Red Flags    | SPF, DKIM, and DMARC checks failed     |
| 6 | Reply-to Mismatch   | Different reply-to domain              |
| 7 | Grammar Issues      | Poor language and formatting           |
| 8 | Generic Greeting    | "Dear Customer" (not personalized)     |

---

##  Tools Used

- Google Admin Toolbox – Header Analyzer
- Manual inspection (email structure, links, and grammar)

---

##  Conclusion

This email is a **phishing attempt** aimed at stealing user credentials. Multiple red flags confirm malicious intent.

---


