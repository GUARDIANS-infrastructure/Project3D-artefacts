# UAT Report: RDDP UAT 01: Cohort-level beacon on RDDP datasets

**Tester:** Informatician A

**Date:** 2025-11-27

**Environment:** prod

**Version:** v2.0-478214b

## Task list

> Follow instructions, assign a status (PASS, PARTIAL, FAIL, NA), add comment when appropriate

- **TS-01:** Access the beacon API at [https://beacon.dsp.garvan.org.au/api/info](https://beacon.dsp.garvan.org.au/api/info)
  - Status: PASS
  - Comment: Access API endpoint using Chrome web browser
- **TS-02:** Record `environment`
  - Status: PASS
  - Comment: Found at `response.environment`
- **TS-03:** Record `version`
  - Status: PASS
  - Comment: Found at `response.version`
- **TS-04:** Inspect organisation
  - Status: PASS
  - Comment: Garvan Institute for Medical Research
- **TS-05:** Inspect contact URL
  - Status: PASS
  - Comment: cardinal @ CPG
- **TS-06:** Access cohorts endpoint at [https://beacon.dsp.garvan.org.au/api/cohorts](https://beacon.dsp.garvan.org.au/api/cohorts)
  - Status: PASS
  - Comment: Access API endpoint using Chrome web browser
- **TS-07:** Inspect number of cohorts
  - Status: PASS
  - Comment: Found at `responseSummary.numTotalResults` - currently 7
- **TS-08:** Inspect cohorts' names
  - Status: PASS
  - Comment: Found at `response.collections.name` - for each cohort
- **TS-09:** Inspect number of participants per cohort
  - Status: PASS
  - Comment: Found at `response.collections.cohortSize` - for each cohort

## Test logs

> Provide additional details, comments or suggestions if needed

- Beacon response display `apiVersion` that is the version of the beacon specification followed, and `version` that is the current version of the beacon node. That is confusing for the user.

- The field `response.organization.name` is currently "Garvan Institute for Medical Research" while it should be "Garvan Institute **of** Medical Research" (note that the description is correct). Issue reported [#4](https://github.com/Garvan-Data-Science-Platform/beacon2-pi-api/issues/4)
