# UAT Report: CTRL UAT 01: Researcher onboarding

**Tester:** Researcher A

**Date:** 2026-03-26

**Environment:** uat

**Version:** v1.2.2_2a25501

## Context

A 1h live session has been arranged with Researcher A. During this session, CTRL dev team facilitated account creation and provided a walkthrough of the CTRL platform’s core features.

The primary objectives of this live session were:

- User Acceptance Testing (UAT): To observe researcher interaction with the platform and gather professional feedback.
- Onboarding: To assist researchers in navigating the interface and initiating their first study.

Please note that the session has been recorded. The present document is a digest of what happened during the session.

## Actions

### Garvan admin invites one primary researcher as study admin.

- A CTRL Organizaton admin login to CTRL UAT instance, on the admin portal, at <https://admin.ctrluat.dsp.garvan.org.au>.
- The admin use AAF as identity provider
- The admin navigate to Admin Panel > Admin Users, and click on "Create"
- The admin fill "First Names", "Last Name", "Email", select the role "Study Admin", and click on "Save"

> The researcher received an email with a link to register into CTRL admin portal.

### Garvan admin create a new study for the researcher

- The organization admin navigate to Admin Panel > Manage Studies, click on "New Study"
- The admin fill the study name and click "Create"
- The admin navigate to Admin Panel > Admin Users, Click on "Edit" on the researcher row, and check the newly created study, and click on "Save"

> The researcher has now permission to manage the selected study

### Researcher gain access to CTRL admin portal

- The researcher received an email with a link to reset password for CTRL admin portal.
- The researcher follow the link and set their password
- The researcher encounter an issue (see I1)
- The organization admin direct the researcher toward the correct URL to continue the onboarding
- The researcher login to the admin portal using AAF, selecting their institution, and performing MFA
- The researcher then land on the Surveys page

> The researcher can now access CTRL admin portal

### Researcher invites additional researcher(s) as study admin

- The researcher navigate to Admin Panel > Admin Users, and click on "Create"
- The admin fill "First Names", "Last Name", "Email", select the role "Study Admin", and click on "Save"

> The second researcher received the invitation email

### Configuring study-specific settings (e.g. name, logos, ...)

- The researcher has access to the Admin Panel > Manage Studies page
- The researcher edit the study name and description
- The researcher navigate to the study advanced option and set a "contact us" email

> Note that the resarcher could set a logo for the study at this step, but they did not test that feature
>
> Note that we discussed REDCap integration and advised not to link real world data in the UAT instance.

### Drafting the initial consent form

- The researcher navigate to Surveys and click on the edit button for the current draft
- The researcher click on "New step", edit the title and the description
- The researcher click on "+ checkbox question" and edit the question text and the tooltip
- The researcher also explore the question advanced options incuding marking a question as mandatory
- The researcher click on "+ multi-choice question" and edit the question text, the tooltip, and the choices

## Feedbacks and issues

UA-1: following the invitation process the researcher encounter an error "error login in: User is not a participant"
> This is a known issue due to wrong URL provided in the invitation email. The researcher is directed to the participant portal instead of the admin portal.
> See [#695](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/695)

UA-2: On the Manage study page, when editing study name or description, the researcher password manager suggest to select a username
> See [#821](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/821)

[13min]
