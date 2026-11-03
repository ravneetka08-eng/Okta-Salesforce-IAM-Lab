
# Test results

| Test ID | Date | Test identity | Action | Expected result | Actual result | Pass/Fail | Evidence file |
|---|---|---|---|---|---|---|---|
| T01 | 03 Nov 2026 | Test Marketing user | Launch Salesforce from Okta | SSO succeeds if corresponding Salesforce user is properly configured | Salesforce SSO error observed; successful SAML authentication not confirmed | Fail (attempt) | `evidence/salesforce/02-sso-error.png` |
| T02 | 01 Nov 2026 | Test HR user | Check Salesforce assignment | Salesforce application not assigned in Okta | Salesforce application tile absent from Okta dashboard; assignment status not independently confirmed | Partially verified | `evidence/okta/06-salesforce-app-not-visible.png` |
| T03 | 01 Nov 2026 | Test Marketing user | Remove group membership and refresh Okta dashboard | Salesforce application assignment disappears | Screenshots show Salesforce tile present and absent; group removal as the cause not independently confirmed | Partially verified | `evidence/okta/05-salesforce-app-assigned.png`, `evidence/okta/06-salesforce-app-not-visible.png` |
| T04 | TBD | Test Marketing user | Check existing Salesforce session after access removal | Record whether the existing Salesforce session remains active or is revoked | Test executed; actual session behaviour to be documented | Completed — outcome pending | Evidence pending |
| T05 | TBD | Test users | Review Okta System Log | Relevant authentication and application access events visible | System Log reviewed; specific events to be documented | Completed — findings pending | Evidence pending |
