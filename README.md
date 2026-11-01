# Okta–Salesforce Identity and Access Management Lab

## Overview
Portfolio lab for learning identity administration, group-based application assignments, MFA policy configuration, and SAML 2.0 SSO between Okta (identity provider) and Salesforce (service provider).

**Status:** In progress. Features below are planned verification tasks, not claims of completed implementation.

## Architecture
- **Okta:** Identity provider, user/group directory, authentication and app assignments.
- **Salesforce:** Downstream CRM application and service provider; manages its own users, licences, and permissions.
- **SAML 2.0:** Federation for single sign-on; it is not user provisioning.
- **Optional provisioning:** Separate mechanism, only document if actually implemented and verified.

## Planned demonstrations
| Scenario | Evidence | Status |
|---|---|---|
| Create two test identities | `evidence/okta/01-users.png` | Not yet verified |
| Create groups and memberships | `evidence/okta/02-groups.png` | Not yet verified |
| Review MFA/authentication policy | `evidence/okta/03-auth-policy.png` | Not yet verified |
| Configure Salesforce SAML settings | `evidence/salesforce/01-saml-settings.png` | Not yet verified |
| Configure Okta Salesforce integration | `evidence/okta/04-salesforce-saml.png` | Not yet verified |
| Assign Salesforce app to approved group | `evidence/okta/05-group-app-assignment.png` | Not yet verified |
| Positive SSO test | `evidence/tests/01-authorized-sso.png` | Not yet verified |
| Negative access test | `evidence/tests/02-unassigned-user.png` | Not yet verified |
| Remove membership and retest | `evidence/tests/03-access-removal.png` | Not yet verified |
| Review relevant system events | `evidence/tests/04-system-log.png` | Not yet verified |

## Evidence and verification
See [Evidence Checklist](docs/EVIDENCE-CHECKLIST.md) and [Test Results](docs/TEST-RESULTS.md). Replace placeholders only after executing each test.

## Security
All users and organisations in this repository should be synthetic test data. Redact emails, org-specific URLs when sensitive, tokens, passwords, recovery codes, QR codes, session cookies, SAML assertions, private keys and confidential data before publishing. Never commit live credentials.

## Learning context
This is an independent hands-on learning portfolio inspired by an IAM workshop. Document only work personally completed and verified; don't represent workshop demonstrations as your own test results.
