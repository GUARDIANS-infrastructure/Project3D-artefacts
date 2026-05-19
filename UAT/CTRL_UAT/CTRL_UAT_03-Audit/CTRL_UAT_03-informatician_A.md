# UAT Report: CTRL UAT 03: Audit Logs

**Tester:** Informatician A

**Date:** 2026-05-18

**Environment:** uat

**Version:** 1.3.1_78791b1

## Context

As a researcher, I have access to CTRL admin portal so that I can review the actions that affect the studies I am in charge of.

The researcher will first perform a series of actions using CTRL application and then review the audit log section.
 They will ensure that all actions have been recorded and the information provided is sufficient for audit purpose.

## Actions

### Login

- Login using Auth0 (Garvan Okta MFA SSO)
- Log out
- Login using AAF

### Surveys

- View a survey
- View a survey responses
- Export a survey as PDF
- Edit a survey
  - Add a new step
  - Edit step title
  - Edit step description
  - Add checkbox question
  - Add multichoice question
  - Publish the survey

### Participants

- Edit the invitation email title and text
- Invite a participant
- View a participant details
- Edit a participant details
- Export participant survey as PDF
- Revoke an invitation

### Admin Users

(Untested)

### Settings

- Edit Study Settings
  - Add a logo
  - Define primary and secondary colors

### Manage Studies

(Untested)

## Feedback and issues

- I would suggest to reorder the columns as: ID, timestamp, resource, userID, operation, success, detail, body
  - ID and timestamp first as it helps to order chronologically the items
  - Resource and UserID next as it inform on the scope of the items
  - Operation and Success and it inform of the status of the items
  - Details and body last for more informations
  > See [#846](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/846)

- For the success column, instead of true and false, I would display a green badge "succeeded" or a red badge "failed".
  > See [#847](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/847)

- Suggest to have the operation as badges of different colors (not green, not red)
  > See [#848](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/848)

- Is the operation (create, update, delete), synonyms of the request (post, patch, delete) ? if yes no need to duplicate the information.
  > See [#849](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/849)

- Suggest to add ordering (asc/desc on column headers), and filtering (query builder) features
  > See [#850](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/850)

- Resource and Request Details are highly repetitive, unsure what is the purpose of both
  > See [#851](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/851)

- The event recording admin login:
  - why is login a create operation ?
  - userID is not populated
  - provider is present only in the body, hard to review, would be nice to have it as a field.
  - is the "code" sensitive information ?
  > See [#852](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/852)

- Editing a survey is creating a lot of events, on for each field edited. It is good for ausit trail but it add a lot on information on the main list. It would be good to separate the survey events into a different page or tab
  > See [#853](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/853)

- Exporting a survey as PDF is not logged
  > See [#854](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/854)

- Publishing a survey is a create operation, post call with no payload. unexpected combo.
  > See [#855](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/855)

- Editing participant invite (email title and content) is not logged
  > See [#856](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/856)

- Inviting participant is not logged
  > See [#857](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/857)

- The event of participant registration exposes full details without encryption
  > See [#858](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/858)

- The event of admin editing participant details exposes full details without encryption
  > See [#858](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/858)

- The event of participant editing their details exposes full details without encryption
  > See [#858](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/858)

- A participant login to the application generate 2 events, on recording email and *** for password, and another event recording OTP. userID is not recorded, it is not possible to link the 2 events to one participant login action.
  > See [#859](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/859)
