# UAT Report: REMS UAT 03: Feedback

**Tester:** Informatician A

**Date:** 2026-05-19

**Environment:** uat

**Version:** REMS v2.38.1 "Välimerenkatu +1"

## Related GUARDIANS Task

3D-5-8: (REMS) Conduct user acceptance testing to refine functionality and improve user experience.

## User Story

As a data handler, I want to review data access request, so I can request decision from the data access committee.

As a data handler, I want to review data access committee decisions, so I can approve or reject request and inform the requester.

## Actions

### REMS access

- Login using AAF
- Logout

### Application Review

- View application
- Review the application
- Request decision from the DAC members
- Approve or reject the application
- Add comment to notify data access instructions.

## Feedback and issues

- When requesting a decision from the DAC members we need to select them from the email list. The email list shows all user accounts in the REMS system. It would be better if this is reduced to a list of just the DAC members.
  > Issue reported to REMS dev team: [#3388](https://github.com/CSCfi/rems/issues/3388)

- To view any documents attached to the application, it needs to be downloaded first. It would be better if we can preview the attachment from the portal instead and download it only if needed.
