# UAT Report: RDDP UAT 01: Cohort-level beacon on RDDP datasets

**Tester:** Maxime HEBRARD, Team Lead

**Date:** 2025-11-26

**Environment:** test

**Version:** v2.0-478214b

## Task list

> Follow instructions, assign a status (PASS, PARTIAL, FAIL, NA), add comment when appropriate

- **TS-01:** Access the beacon API at [https://dev.beacon.dsp.garvan.org.au/api/info](https://dev.beacon.dsp.garvan.org.au/api/info)
  - Status: PASS
  - Comment: Access API endpoint using Chrome web browser
- **TC-02:** Record `environment`
  - Status: PASS
  - Comment: Found at `response.environment`
- **TC-03:** Record `version`
  - Status: PASS
  - Comment: Found at `response.version`
- **TC-04:** Inspect organisation
  - Status: PASS
  - Comment: Garvan Institute for Medical Research
- **TC-05:** Inspect contact URL
  - Status: PASS
  - Comment: cardinal @ CPG
- **TC-06:** Access cohorts endpoint at [https://dev.beacon.dsp.garvan.org.au/api/cohorts](https://dev.beacon.dsp.garvan.org.au/api/cohorts)
  - Status: PASS
  - Comment: Access API endpoint using Chrome web browser
- **TC-07:** Inspect number of cohorts
  - Status: PASS
  - Comment: Found at `responseSummary.numTotalResults` - currently 7
- **TC-08:** Inspect cohorts' names
  - Status: PASS
  - Comment: Found at `response.collections.name` - for each cohort
- **TC-09:** Inspect number of participants per cohort
  - Status: PASS
  - Comment: Found at `response.collections.cohortSize` - for each cohort

## Test logs

> Provide additional details, comments or suggestions if needed

Beacon response display `apiVersion` that is the version of the beacon specification followed, and `version` that is the current version of the beacon node. That is confusing for the user.
