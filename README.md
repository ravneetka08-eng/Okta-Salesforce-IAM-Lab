# Okta–Salesforce Identity and Access Management Lab

## Overview
Portfolio lab for learning identity administration, group-based application assignments, MFA policy configuration, and SAML 2.0 SSO between Okta (identity provider) and Salesforce (service provider).

**Status:** In progress. Features below are planned verification tasks, not claims of completed implementation.

## Architecture
- **Okta:** Identity provider, user/group directory, authentication and app assignments.
- **Salesforce:** Downstream CRM application and service provider; manages its own users, licences, and permissions.
- **SAML 2.0:** Federation for single sign-on; it is not user provisioning.
- **Optional provisioning:** Separate mechanism, only document if actually implemented and verified.


## Implementation Demonstrations

| Scenario | Evidence | Status |
|---|---|---|
| Create test identities in Okta | `evidence/okta/01-okta-users.png` | Completed — users visible |
| Create groups in Okta | `evidence/okta/02-okta-groups.png` | Completed — groups visible |
| Configure user-group membership | `evidence/okta/03-hr-group-membership.png` | Completed — membership visible |
| Review MFA/authentication policy | Not captured | Configured — evidence pending |
| Configure Salesforce SAML settings | `evidence/salesforce/01-saml-sso-configuration.png` | Completed — configuration captured |
| Configure Okta Salesforce integration | `evidence/okta/04-salesforce-app-integration.png` | Completed — configuration captured |
| Assign Salesforce application to approved users/groups | `evidence/okta/05-salesforce-app-assigned.png` | Partially verified — app visible in dashboard |
| Check Salesforce application visibility for another user | `evidence/okta/06-salesforce-app-not-visible.png` | Observed — app tile absent |
| Positive SSO test | `evidence/salesforce/02-sso-error.png` | Failed attempt — troubleshooting required |
| Salesforce application session | `evidence/salesforce/03-salesforce-session.png` | Observed — SSO method not confirmed |
| Remove group membership and retest | Evidence pending | Tested — access removal verified by user |
| Check existing Salesforce session after access removal | Evidence pending | Tested — session outcome to be documented |
| Review relevant Okta System Log events | Evidence pending | Tested — log findings to be documented |
| Automated Salesforce deprovisioning | Not applicable | Not implemented |

## Evidence and Verification

Screenshots collected during implementation are stored in the
`evidence/` directory.

### Okta Evidence

- User creation and account management.
- Group creation and membership configuration.
- Salesforce application integration.
- Salesforce application visibility in the Okta dashboard.
- Salesforce application absence from another dashboard.

### Salesforce Evidence

- SAML 2.0 Single Sign-On configuration.
- SSO authentication error captured during testing.
- Salesforce application session captured.

### Verification Status

The project demonstrates the configuration of Okta as an
Identity Provider (IdP) and Salesforce as a Service Provider (SP).

The screenshots support the completed configuration activities
and selected application-visibility observations.

However, successful end-to-end SAML authentication has not
yet been confirmed.

The Salesforce session screenshot does not independently
prove that authentication occurred through Okta SAML SSO.

Removing an Okta application assignment does not automatically
deactivate the corresponding Salesforce user account.

Automated Salesforce provisioning and deprovisioning
were not implemented in this project.

### Supporting Documentation

- [Test Results](docs/TEST-RESULTS.md)
- [Evidence Checklist](docs/EVIDENCE-CHECKLIST.md)
- [Evidence Screenshots](evidence/README.md)

### Remaining Validation

- Troubleshoot the Salesforce SSO authentication error.
- Verify successful SAML authentication and identity mapping.
- Confirm application assignment removal following group changes.
- Test Salesforce session behaviour after access removal.
- Review Okta System Log events and capture evidence.

