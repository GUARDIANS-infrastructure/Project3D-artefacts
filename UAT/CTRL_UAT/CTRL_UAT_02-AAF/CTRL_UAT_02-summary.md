# CTRL UAT 02: AAF / AAI solution

**User Story:** [CTRL Story 07: AAI solution integration for CTRL admin (AAF member)](/User_Stories/CTRL_User_Stories/CTRL07-aai_integration_member.md)

## Summary of Results

> ✅ PASS / ⚠️ PARTIAL / ❌ FAIL / Ⓧ N.A.

| Role | TS-01 | TS-02 | TS-03 | TS-04 | TS-05 | TS-06 | TS-07 | Overall Status |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| Researcher A | ✅ | ⚠️(1)(2) | ✅ | ✅(3) | ✅(4) | ✅ | ✅ | **PASS** |

## Key Findings & Blocker Notes

### Comments

1. It is a reset password email, that is odd in the context of a invitation. Issue reported [#]()
2. [solved] The invitation email redirect to the participant portal instead of the admin portal. Issue reported [#695](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/695)
3. Adelaide University is an AAF member
4. Adelaide University enfore MFA via authenticator app
