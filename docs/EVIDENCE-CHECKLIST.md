
# Evidence Checklist

## Okta Configuration

| Evidence ID | Configuration | Description | Status | Evidence file |
|---|---|---|---|---|
| E01 | User management | Test user accounts created in Okta | Captured | `evidence/okta/01-okta-users.png` |
| E02 | Group management | Groups created in Okta | Captured | `evidence/okta/02-okta-groups.png` |
| E03 | Group membership | HR group membership configured | Captured | `evidence/okta/03-hr-group-membership.png` |
| E04 | Salesforce integration | Salesforce application configured in Okta | Captured | `evidence/okta/04-salesforce-app-integration.png` |
| E05 | Application assignment | Salesforce application visible in Okta user dashboard | Captured | `evidence/okta/05-salesforce-app-assigned.png` |
| E06 | Application visibility | Salesforce application absent from Okta user dashboard | Captured | `evidence/okta/06-salesforce-app-not-visible.png` |

## Salesforce Configuration

| Evidence ID | Configuration | Description | Status | Evidence file |
|---|---|---|---|---|
| E07 | SAML SSO | Salesforce SAML Single Sign-On configuration | Captured | `evidence/salesforce/01-saml-sso-configuration.png` |
| E08 | SSO troubleshooting | Salesforce SSO error during authentication attempt | Captured | `evidence/salesforce/02-sso-error.png` |
| E09 | Salesforce session | Salesforce Chatter session visible; SSO authentication method not confirmed | Captured | `evidence/salesforce/03-salesforce-session.png` |

## Additional Evidence Required

- [ ] Successful Okta-to-Salesforce SAML SSO login
- [ ] Verified Salesforce identity matching using NameID
- [ ] Confirmed application assignment removal after group change
- [ ] Existing Salesforce session behaviour after access removal
- [ ] Okta System Log authentication events
- [ ] Okta System Log application assignment events

## Evidence Handling

- Screenshots must not expose passwords, tokens, secrets, or private keys.
- Sensitive tenant information should be redacted where appropriate.
- Original screenshots should be retained privately if needed.
- Test outcomes must be supported by captured evidence.
