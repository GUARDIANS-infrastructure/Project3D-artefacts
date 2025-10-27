# CTRL Epic 07: AAI solution integration for CTRL admin (AAF members)

## Related GUARDIANS Task

3D-4-2: Defined core use-cases, requirements, acceptance criteria, and stub integration tests for integration with AAI solution (GUARDIANS project 2B), available on a platform like GitHub.

## User Story

- As a study admin, I want to login to CTRL admin portal using my institutional affiliation so that I can manage study securely.

## Context

- Study admin is invited to CTRL admin portal by the sys admin or another tudy admin.

## Acceptance Criteria

- Study admin can login to CTRL admin portal.
- Study admin use their institutional email to login.
- Institution of the study admin is member of AAF.
- Study admin use Multi Factor Authentication (MFA) to login.
- CTRL login request include Authentication Context Class Reference (`arc_value`) of AAL2 (`http://idmanagement.gov/ns/assurance/aal/2`), standard NIST identifier which requires MFA, as mandatory (`essential:true`).
- AAI login response specify the Authentication Methods Reference (`amr`) used.
- `amr` acceptable by Garvan [to be determined].
