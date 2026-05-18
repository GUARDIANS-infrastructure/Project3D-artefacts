# UAT Report: RENS UAT 02: Audit Logs

**Tester:** Informatician A

**Date:** 2026-04-02

**Environment:** uat

**Version:** REMS v2.38.1 "Välimerenkatu +1"

## Context

As a researcher, I have access to REMS application and API so that I can review the actions related to the dataset that I manage.

REMS provides 3 sources of information that could be considered logs, and can be used to monitor activity on the application.

- a downloadable report: This is a CSV file that lists all applications, including applicant name, submission date, and application status.
- an audit trail: This is an API endpoint that lists server events including timestamp, api path, method, userid and request status.
- an event history: This is a list of events displayed in the REMS UI including user, action, comments and attachment.

The first two (downloadable report, and api endpoint) are mentioned in the REMS documentation.
The event history is visible in the UI.

## Feedback and issues

- The three sources of events record very different types of information and it is hard to have an holistic view of the activity on the application.
- The audit trail API is flooded with `get` requests related to server health checks and image transfer. It is hard to find relevant actions in the response.
- The audit trail API records the timestamp, endpoint and user but does not record any information related to the action performed (no request body). It has limited usefulness in my opinion.
- There is no obvious way to link the report to the audit trail. The ID numbers do not match and no other application identifiers or other match information is provided.
- The event history contain useful information and is presented in an easy-to-understand manner (with interpretation of events and attribution to the name of the person responsible e.g. "Hannah Handler redacted attachements, New Attachments replace the redacted attachments." with the ability to access the different documents; or "Diana Decider added a remark"). Individual events can be hidden or maximised. This is the most useful view of the three options. However it is hard to search within events, or link these events to the other other sources (API or downloadable report).

- It would be excellent if the three logs could be harmonised, and additional search functionality added to the UI.
