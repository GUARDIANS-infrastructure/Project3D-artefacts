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
- The researcher also explore the question advanced options incuding marking a question as mandatory and link an ontology term
- The researcher click on "+ multi-choice question" and edit the question text, the tooltip, and the choices
- The researcher click on "+ subheading" and edit the text of the heading
- The researcher re-order the questions and subheadings by drag and drop each block
- The researcher create multiple steps for the survey
- The researcher re-order the survey step using the cog menu
- The researcher publish the survey

### Invite a participant

- The researcher navigate to Participants
- The researcher select the study of interest (in case of multiple study available)
- The researcher click on "invite participants"
- The researcher can edit the invitation message and see a preview of the email received by the participant
- The researcher fill participant email list
- The researcher send invitations
- The researcher can now inspect the participant with pending invitations
- The researcher revoque an invite (that was sent to a wrong email)

## Feedbacks and issues

UA-1: following the invitation process the researcher encounter an error "error login in: User is not a participant"
> This is a known issue due to wrong URL provided in the invitation email. The researcher is directed to the participant portal instead of the admin portal.
> See [#695](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/695)

UA-2: On the Manage study page, when editing study name or description, the researcher password manager suggest to select a username
> See [#821](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/821)

UA-3: in the Survey page, the modal displayed when publishing a survey in unclear "Once you publish a version, it can't be edited" raze a worry that the researcher needs to create a new survey from scratch. I should be rephrase to communicate that the version is locked but further edit is doable and will create a new version.
> See [#833](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/833)

UA-4: in the Survey page, when admin try to publish the survey, It seems to have form validation blocking the publishing but no message is shown to the user.
> See [#834](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/834)

UA-5: When creating a multi choice questions, the need to click on th "+" button to add a choice is not ideal UX, user would expect to press enter and have the cursor ready in a new field.
> See: [#835](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/835)

UA-6: When creating a multi choice questions, The UI of the choices is inconsistant. i.e. white space between the choices and distance to the "+" button changes over time
> See [#836](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/836)

UA-7: A multi-choice question should be able to set as mandatory question too. If the user did not review the question, nothing is ticked. The participant is forced to choose one choice before submitting the survey.
> See [#837](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/837)

UA-8: It would be nice to have a pre-filed list of state or country... In the context of question like "where do you leave". Could we use an ontology ?
> See [#838](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/838)

UA-9: Current multi-choice question is radio button type (only one choice ticked). There should be a multi-choice option checkbox type (multiple choices ticked).
> See [#839](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/839)

UA-10: Need to add a free text entry for the responses. Example of gender question: he/she or specify "?" with option for validation rules (email, phone number, date, member card...)
> See [#840](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/840)

UA-11: For multi-choice question with only one answer allowed, depending of the number of choices, suggest to use dropdown
> See [#841](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/841)

UA-12: Expression of interest to have a platform that can manage participant survey. i.e. recontacting the participant & asking a set of questions that are not consent but questionnaire. i-Considering building the survey in CTRL and store the response in CTRL. ii-Considering building the survey in REDCap and store the responses in REDCap. iii-Considering embedded the questionnaire in CTRL but store the responses in REDCap. Either way it would be nice to have a notification of questionnaire status within CTRL, and delegate participant management to CTRL (emails, follow up, dashboard...).
> See [#842](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/842)

UA-13: It would be usefull for the admin to be able to visualized the survey the way it appears to the participant
> See [#665](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/665)

UA-14: When editing a survey, there is no button to go back to the survey page, the only way out is through the menu. User expect a "back" button of some sort
> See [#843](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/843)

UA-15: It would be nice to be able to style the survey description, using markdown for example
> See [#844](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/844)

UA-15: It would be nice to be able to style the invite email, using markdown for example
> See [#741](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/741)

UA-16: Wish to export the list of participant invites
> See [#845](https://github.com/Garvan-Data-Science-Platform/ctrl/issues/845)
