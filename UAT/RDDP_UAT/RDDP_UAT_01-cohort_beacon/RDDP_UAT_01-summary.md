# RDDP UAT 01: Cohort-level beacon on RDDP datasets

**Epic:** [RDDP Epic 01: Cohort-level beacon on RDDP datasets](/RDDP_epics/RDDP01-cohort_beacon.md)

## Summary of Results

> ✅ PASS / ⚠️ PARTIAL / ❌ FAIL / Ⓧ N.A.

| Role | TC-01 | TC-02 | TC-03 | TC-04 | TC-05 | TC-06 | TC-07 | TC-08 | TC-09 | Overall Status |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---           |
| Informatician A | ✅ | ✅ | ✅(1) | ✅(2) | ✅ | ✅ | ✅ | ✅ | ✅ | **PASS** |

## Key Findings & Blocker Notes

### Comments

1. Beacon response display `apiVersion` that is the version of the beacon specification followed, and `version` that is the current version of the beacon node. That is confusing for the user.
2. The field `response.organization.name` is currently "Garvan Institute for Medical Research" while ut should be "Garvan Institute **of** Medical Research" (note that the description is correct). Issue reported [#4](https://github.com/Garvan-Data-Science-Platform/beacon2-pi-api/issues/4)
