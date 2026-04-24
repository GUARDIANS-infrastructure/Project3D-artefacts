# UAT Report: CTRL UAT 02: AAF / AAI solution

> Name and email will be recorded in a separate document

**Tester:** Researcher A

**Date:** 2026-03-26

**Environment:** UAT

**Version:** v1.2.2_2a25501

## Task list

> Follow instructions, assign a status (PASS, PARTIAL, FAIL, NA), add comment when appropriate

- **TS-01** Receive an e-mail with a link to register into CTRL admin portal
  - Status: PASS
  - Comment:
- **TS-02** Follow the link in the email
  - Status: PARTIAL
  - Comment:
    - It is a reset password email, that is odd in the context of a invitation
    - the email redirect to the participant portal instead of the admin portal
- **TS-03** From the admin portal, select Australian Access Federation
  - Status: PASS
  - Comment:
- **TS-04** Select current affiliation
  - Status: PASS
  - Comment: Adelaide University is an AAF member
- **TS-05** Follow instruction to login using affiliation credentials
  - Status: PASS
  - Comment: Adelaide University enfore MFA via authenticator app
- **TS-06** Approve CILogon terms & conditions
  - Status: PASS
  - Comment:
- **TS-07** Confirm access to CTRL admin portal
  - Status: PASS
  - Comment:

## Test logs

> Provide additional details, comments or suggestions if needed
