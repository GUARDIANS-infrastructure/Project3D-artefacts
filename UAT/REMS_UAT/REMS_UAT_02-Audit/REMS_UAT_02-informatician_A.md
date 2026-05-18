# UAT Report: RENS UAT 02: Audit Logs

**Tester:** Informatician A

**Date:** 2026-04-02

**Environment:** uat

**Version:** REMS v2.38.1 "Välimerenkatu +1"

## Context

As a researcher, I have access to REMS application and API so that I can review the actions related to the dataset that I manage.

REMS provide 3 sources of informations that could be consider logs, and be used to monitor activity on the application.

- a downloadable report: It is a CSV file that list all applications, including applicant name, submission date, and application status.
- an audit trail: It is an API enpoint that list server events including timestamp, api path, method, userid and request status.
- an event history: It is a list of events displayed in the REMS UI including user, action, comments and attachment.

## Feedback and issues

- The three sources of events record very differnt type of information and it is hard to have an holistic view of the activity on the application.
- The audit trail API is flooded with get request related to server health checks and image transfer. It is hard to find relevant actions in the response.
- The audit trail API record API the timestamp, endpoint and user but to not record any information related to the action performed (no request body). It has limited usefulness IMO.
- There is no obvious way to link the report to the audit trail. No application ID or other match information.
- The event history contain usefull information, but it is hard to search or link to other sources.
