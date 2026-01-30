# UAT Report: RDDP UAT 01: Cohort-level beacon on RDDP datasets

> Name and email will be recorded in a separate document

**Tester:** Clinician A

**Date:** 2026-01-08

**Environment:** prod

**Version:** v2.0.0

## Task list

> Follow instructions, assign a status (PASS, PARTIAL, FAIL, NA), add comment when appropriate

- **TS-01:** Access the beacon API at [https://beacon.dsp.garvan.org.au/api/info](https://beacon.dsp.garvan.org.au/api/info)
  - Status: PASS
  - Comment: using Chrome
- **TC-02:** Record `environment`
  - Status: PASS
  - Comment:
- **TC-03:** Record `version`
  - Status: PASS
  - Comment:
- **TC-04:** Inspect organisation
  - Status: PASS
  - Comment:
- **TC-05:** Inspect contact URL
  - Status: PASS
  - Comment:
- **TC-06:** Access cohorts endpoint at [https://beacon.dsp.garvan.org.au/api/cohorts](https://beacon.dsp.garvan.org.au/api/cohorts)
  - Status: PASS
  - Comment: using Chrome
- **TC-07:** Inspect number of cohorts
  - Status: PASS
  - Comment: numTotalResults
- **TC-08:** Inspect cohorts' names
  - Status: PASS
  - Comment: in ‘name’. Not sure if possible to put this first in the dict of each collection?
- **TC-09:** Inspect number of participants per cohort
  - Status: PASS
  - Comment: in both ‘cohortSize’ and ‘availabilityCount’, or is ‘availabilityCount’ different?

## Test logs

> Provide additional details, comments or suggestions if needed

Is it possible to include the HPO codes in ‘distribution’ somehow? Or will these appear nicer on a UI platform for example?
