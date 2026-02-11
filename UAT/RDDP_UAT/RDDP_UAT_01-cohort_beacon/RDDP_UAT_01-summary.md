# RDDP UAT 01: Cohort-level beacon on RDDP datasets

**Epic:** [RDDP Epic 01: Cohort-level beacon on RDDP datasets](/RDDP_epics/RDDP01-cohort_beacon.md)

## Summary of Results

> ✅ PASS / ⚠️ PARTIAL / ❌ FAIL / Ⓧ N.A.

| Role | TS-01 | TS-02 | TS-03 | TS-04 | TS-05 | TS-06 | TS-07 | TS-08 | TS-09 | Overall Status |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| Informatician A | ✅ | ✅ | ✅(1) | ✅(2) | ✅ | ✅ | ✅ | ✅ | ✅ | **PASS** |
| Informatician B | ✅ | ✅ | ✅ | ✅ | ✅(3) | ✅ | ✅ | ✅ | ✅ | **PASS** |
| Informatician C | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅(4) | ✅ | **PASS** |
| Clinician_A | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅(5) | ✅(6) | **PASS** |
| Clinician_B | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | **PASS** |

## Key Findings & Blocker Notes

### Comments

1. Beacon response display `apiVersion` that is the version of the beacon specification followed, and `version` that is the current version of the beacon node. That is confusing for the user.
2. [solved] The field `response.organization.name` is currently "Garvan Institute for Medical Research" while it should be "Garvan Institute **of** Medical Research" (note that the description is correct). Issue reported [#4](https://github.com/Garvan-Data-Science-Platform/beacon2-pi-api/issues/4)
3. Suggest updating the display name from RDPP to CaRDinal. "name": "RDDP cohort-level beacon" to "name": "CaRDinal cohort-level beacon". Suggestion reported [#5](https://github.com/Garvan-Data-Science-Platform/beacon2-pi-api/issues/5)
4. Noticed a few `\n` line breaks in the cohort description; removing them would make it read more smoothly. Suggestion reported [#6](https://github.com/Garvan-Data-Science-Platform/beacon2-pi-api/issues/6)
5. Clarify whether and how HPO codes associated with each cohort could be represented in the `distribution` field versus being surfaced only via a downstream UI.
6. Clarify the intended semantic difference between `cohortSize` and `availabilityCount` for the number of participants per cohort.
