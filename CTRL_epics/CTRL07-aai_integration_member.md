# CTRL Epic 07: AAI solution integration for CTRL admin (AAF member)

## Related GUARDIANS Task

3D-4-2: Defined core use-cases, requirements, acceptance criteria, and stub integration tests for integration with AAI solution (GUARDIANS project 2B), available on a platform like GitHub.

## User Story

- As a study admin, I want to login to CTRL admin portal using my institutional credentials, so that I can manage study securely.

## Context

- Study admin is invited to CTRL admin portal by the sys admin or another study admin.
- As CTRL admin portal contains Personally Identifiable Information (PII), security best practices (defined by NIST) and Garvan IT policies required strong Multi Factor Authentication (MFA) for login.

## Acceptance Criteria

- [ ] Study admin from an AAF member organisation can login to CTRL admin portal.
- [ ] Study admin use Multi Factor Authentication (MFA) to login.
- [ ] CTRL login request include Authentication Context Class Reference (`arc_value`) of AAL2 (`http://idmanagement.gov/ns/assurance/aal/2`), standard NIST identifier which requires MFA, as mandatory (`essential:true`).
- [ ] AAI login response specify the Authentication Methods Reference (`amr`) used.
- [ ] `amr` acceptable by Garvan [to be determined].
