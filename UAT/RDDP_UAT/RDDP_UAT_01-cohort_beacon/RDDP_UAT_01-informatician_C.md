# UAT Report: RDDP UAT 01: Cohort-level beacon on RDDP datasets

> Name and email will be recorded in a separate document

**Tester:** Informatician C

**Date:** 2025-12-19

**Environment:** prod

**Version:** v2.0.0

## Task list

> Follow instructions, assign a status (PASS, PARTIAL, FAIL, NA), add comment when appropriate

- **TS-01:** Access the beacon API at [https://beacon.dsp.garvan.org.au/api/info](https://beacon.dsp.garvan.org.au/api/info)
  - Status: PASS
  - Comment: using Chrome
- **TC-02:** Record `environment`
  - Status: PASS
  - Comment: found at "environment"
- **TC-03:** Record `version`
  - Status: PASS
  - Comment: found at "apiVersion"
- **TC-04:** Inspect organisation
  - Status: PASS
  - Comment: "id": "Garvan", "name": "Garvan Institute of Medical Research"  
- **TC-05:** Inspect contact URL
  - Status: PASS
  - Comment: "contactUrl": "mailto:cardinal@populationgenomics.org.au"
- **TC-06:** Access cohorts endpoint at [https://beacon.dsp.garvan.org.au/api/cohorts](https://beacon.dsp.garvan.org.au/api/cohorts)
  - Status: PASS
  - Comment: using Chrome
- **TC-07:** Inspect number of cohorts
  - Status: PASS
  - Comment: found at "numTotalResults": 8
- **TC-08:** Inspect cohorts' names
  - Status: PASS
  - Comment: found at “name"
- **TC-09:** Inspect number of participants per cohort
  - Status: PASS
  - Comment: found at "cohortSize"

## Test logs

> Provide additional details, comments or suggestions if needed

Noticed a few \n line breaks in the cohort description; removing them would make it read more smoothly.
