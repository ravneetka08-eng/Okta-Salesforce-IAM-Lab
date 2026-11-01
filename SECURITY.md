# Security and publishing guidance

This repository must contain only lab-safe material. Do not commit:
- passwords, OTP seeds, MFA QR codes, recovery codes, access/refresh tokens, API keys, client secrets
- session cookies, raw SAML responses/assertions, private keys, sensitive certificates or identity-provider metadata
- personal email addresses, real employee records, confidential customer data
- unredacted tenant URLs or unique identifiers if you prefer not to expose your lab tenant

Before each commit, visually inspect all screenshots and review `git diff --cached`.
