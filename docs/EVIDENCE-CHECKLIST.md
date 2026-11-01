# Screenshot capture checklist

Capture only **your own** lab, after performing each action. Name files as shown in the README.

1. Okta > Directory > People: two synthetic users (redact identifiers if needed).
2. Okta > Directory > Groups: two groups and their members.
3. Okta > Security > Authentication Policies: relevant policy and requirements; never expose secrets.
4. Salesforce > Setup > Single Sign-On Settings: SAML enabled and configuration (redact org-specific URLs/certificates as appropriate).
5. Okta > Applications > Salesforce: SAML sign-on configuration (redact sensitive values).
6. Okta > Groups > Applications: group-to-Salesforce assignment.
7. Browser private session: assigned test user successfully reaches Salesforce through Okta (capture landing page, not tokens).
8. Separate private session: unassigned user cannot access Salesforce via Okta; note exact observed outcome (missing tile, access denied, etc.).
9. Remove group membership and repeat test: show assignment removal and resulting behaviour. A missing bookmark tile alone does not prove Salesforce sessions were revoked.
10. Okta System Log: event type, result, timestamp and synthetic user, with sensitive identifiers redacted.

For each screenshot, record date, action, expected result, actual result, and whether it passed in TEST-RESULTS.md.

## Additional strong evidence
- A simple architecture diagram showing Okta as IdP and Salesforce as separate SP.
- An access matrix listing test users, groups, intended app assignments, and actual outcomes.
- One failed sign-in troubleshooting example with resolution, if encountered.
- A short limitations section: app assignment is not the same as Salesforce authorisation; SAML SSO is not SCIM provisioning; removing an Okta tile does not necessarily terminate existing Salesforce sessions.
