# CTRL Epic 01: Assign DUO Codes to Survey Questions

## Related GUARDIANS Task

3D-5-4: Conduct user acceptance testing to refine functionality and improve user experience

## User Story

As a study admin, I want survey question to be assigned with DUO codes so that data release logic can be automated in ELSA.

## Context

Options we could consider:

- Provide a collection of pre-written questions that already have DUO codes that the user can add to their survey
- Prompt user to select a DUO code for a question in the survey builder
  - Build a UI for navigating all possible DUO codes
  - Use LLM for suggesting DUO code based on question text

## Acceptance Criteria

- Survey questions can be assigned DUO codes in the backend
- User can easily see whether a DUO code has been assigned to a question, and if so which one
- There is process in the admin portal for the study admin to assign DUO codes to survey questions
