# Lab 3: Phishing Email Analysis
**Context**: Completed using educational examples from Phishbox.org
**Time to Complete**: 30 minutes

---

## What I Did
- Reviewed real-world phishing email examples to identify common social engineering indicators.
- Examined sender addresses, domain names, and email content to spot spoofing attempts.
- Checked for deceptive links, urgent language, and suspicious requests.
- Analysed email authentication concepts including SPF, DKIM, and DMARC to understand how legitimate emails are verified and how spoofed ones can be detected.
- All work conducted using publicly available educational resources.

---

## Email 1 — Spoofed Sender (DocuSign)
**Red Flags Identified:**
- Fake domain**: Claims to be from DocuSign but uses an unrelated domain after the @ symbol
- Misleading content**: Claims to contain a PDF document but asks to "Confirm Account" instead
- Brand impersonation**: Uses a trusted company name to appear legitimate
- No personalisation**: Real DocuSign emails always address you by your full name

---

## Email 2 — Deceptive Domain (Airbnb)
**Red Flags Identified:**
- Typosquatting**: Uses a lookalike domain — deliberate character substitution to trick the eye
- Fear and urgency**: Mentions an unexpected charge to create pressure to click before thinking
- Deceptive links**: Button text hides the true destination URL — always hover to check before clicking
- Fake credibility details**: Includes real-sounding address and legal text to appear trustworthy, but the sender domain reveals it is fake

---

## Email Authentication Concepts — SPF, DKIM & DMARC
Even without a header screenshot, I examined how email authentication works:

- SPF (Sender Policy Framework)** — Checks if the sending server is authorised to send email from that domain. If SPF fails, the email likely did not come from where it claims.
- DKIM (DomainKeys Identified Mail)** — Adds a digital signature to prove the email was not altered in transit. Missing signature = high risk of tampering.
- DMARC (Domain-based Message Authentication)** — Tells receiving servers what to do if SPF or DKIM fail. If DMARC also fails, the domain owner has not authorised this email to be sent from elsewhere.

> **Conclusion**: When SPF, DKIM, or DMARC fail together, the email is almost certainly spoofed — regardless of how convincing the display name or email content looks.

---

## Key Concepts Demonstrated

### Spoofed Sender Address
Attackers change the display name to match a trusted company (like DocuSign or Airbnb), but the actual email address after the @ symbol reveals the deception. **Always check the full domain — not just the display name.**

### Typosquatting
Slight misspellings, character swaps, or unusual domain endings trick the eye. Read the domain name carefully — `airbnb.com` ≠ `a1rbnb.cc`.

### Urgency and Fear Tactics
"Account suspended", "Payment due", "Action required" — attackers create pressure so you click before verifying. Legitimate organisations do not demand urgent action this way.

---

## What I Learned
- How to systematically examine an email for signs of phishing — sender first, then content, then links.
- Why checking the full sender domain is more reliable than just the display name.
- How SPF, DKIM and DMARC work together to detect spoofed emails.
- Common social engineering tactics: urgency, impersonation, deceptive links, and typosquatting.
- Always hover over links before clicking to check where they actually go — and if in doubt, do NOT click.
