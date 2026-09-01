# Lab 2: Phishing Email Analysis
**Context**: Completed using educational examples from Phishbox.org
**Time to Complete**: 30 minutes

---

## What I Did
- Reviewed real-world phishing email examples to identify common social engineering indicators.
- Examined sender addresses, domain names, and email content to spot spoofing attempts.
- Checked for deceptive links, urgent language, and suspicious requests.
- Analysed email authentication headers including SPF, DKIM, and DMARC to verify email legitimacy.
- All work conducted using publicly available educational resources.

---

## Email 1 — Spoofed Sender (DocuSign)
**Red Flags Identified:**
- Fake domain — claims to be from DocuSign but uses an unrelated domain
- Misleading content — claims to contain a PDF but asks to confirm an account instead
- Impersonation — uses a trusted brand name to appear legitimate
- No personalisation — real emails always address you by your actual name

---

## Email 2 — Deceptive Domain (Airbnb)
**Red Flags Identified:**
- Typosquatting — uses a lookalike domain with a deliberate character substitution
- Fear and urgency — mentions an unexpected charge to create pressure to click
- Deceptive links — button text hides the true destination URL
- Fake credibility — includes real-sounding details to appear trustworthy

---

## Email 3 — Header Authentication Analysis
**SPF, DKIM & DMARC Results:**
- SPF = FAIL — sending server is not authorised by the claimed domain
- DKIM = NONE — no digital signature; email could have been altered
- DMARC = FAIL — domain policy does not prevent spoofing
- Conclusion — email is spoofed; it appears to come from one source but originates from elsewhere

---

## Key Concepts Demonstrated

### Spoofed Sender Address
Attackers change the display name to match a trusted company, but the actual email address reveals the deception. Always check the full domain after the @ symbol.

### Typosquatting
Slight misspellings or swapped characters in domain names trick people into thinking it is the legitimate website. Read the domain name carefully before trusting it.

### Urgency and Fear Tactics
Account suspended, payment due, action required within hours — attackers create pressure so you click before thinking. Legitimate organisations do not demand urgent action this way.

### Email Authentication Protocols
- SPF checks if the sending server is allowed to send from that domain
- DKIM verifies the email has not been altered in transit
- DMARC tells receiving servers what to do if SPF or DKIM fail
- All three failing together is a strong sign the email is spoofed

---

## What I Learned
- How to systematically examine an email for signs of phishing.
- Why the full sender domain is more reliable than the display name.
- How SPF, DKIM and DMARC work together to detect spoofing.
- Common social engineering tactics: urgency, impersonation and deceptive links.
- Always hover over links before clicking to check where they actually go.
