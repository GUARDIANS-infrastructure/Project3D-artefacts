# UAT Report: RDDP UAT 01: Cohort-level beacon on RDDP datasets

> Name and email will be recorded in a separate document

**Tester:** Informatician B

**Date:** 2025-12-19

**Environment:** prod

**Version:** v2.0.0

## Task list

> Follow instructions, assign a status (PASS, PARTIAL, FAIL, NA), add comment when appropriate

- **TS-01:** Access the beacon API at [https://beacon.dsp.garvan.org.au/api/info](https://beacon.dsp.garvan.org.au/api/info)
  - Status: PASS
  - Comment: Chrome
- **TC-02:** Record `environment`
  - Status: PASS
  - Comment: "environment": "prod"
- **TC-03:** Record `version`
  - Status: PASS
  - Comment: "apiVersion": "v2.0.0"
- **TC-04:** Inspect organisation
  - Status: PASS
  - Comment: "organization": { "id": "Garvan", "name": "Garvan Institute of Medical Research" }  
- **TC-05:** Inspect contact URL
  - Status: PASS
  - Comment: "contactUrl": "mailto:cardinal@populationgenomics.org.au"
- **TC-06:** Access cohorts endpoint at [https://beacon.dsp.garvan.org.au/api/cohorts](https://beacon.dsp.garvan.org.au/api/cohorts)
  - Status: PASS
  - Comment: Chrome
- **TC-07:** Inspect number of cohorts
  - Status: PASS
  - Comment: "numTotalResults": 8
- **TC-08:** Inspect cohorts' names
  - Status: PASS
  - Comment: “response.collections.name"
- **TC-09:** Inspect number of participants per cohort
  - Status: PASS
  - Comment: "response.collections.cohortSize"

## Test logs

> Provide additional details, comments or suggestions if needed

Suggest updating the display name from RDPP to CaRDinal
"name": " RDDP cohort-level beacon" to "name": "CaRDinal cohort-level beacon"
