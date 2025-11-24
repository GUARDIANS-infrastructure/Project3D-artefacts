# Project3D-artefacts

This repository contains project artefacts such as user stories and diagrams for GUARDIANS Project 3D coordinated by the Garvan Institute of Medical Research.

## GUARDIANS

The GUARDIANS project (human Genomics Uplift for Australia through Research Data Infrastructure At National Scale) is a National initiative led by Australian BioCommons and funded by NCRIS through Bioplatforms Australia. It aim to empower Australian researchers to easily and securely discover, access, and analyze human genomics data across national infrastructure, using the latest tools and resources.

![Guardians user journey.png](./docs/Guardians_user_journey.png)

## Project 3D: Scalable, Open and Connected Genomics Infrastructure

Under this national grant, Garvan is leading a flashship project that is composed of a few different tools.

- Dynamic Consent Platform: CTRL
- Resource Entitlement Platform: REMS
- Data Release Platform: Elsa data
- Rare Disease Diagnostic Platform: CaRDinal

The goal of the flagship project is to deploy the different tools on Garvan infrastructure and build interaction between them. In the national context, the approach is modular and each institution can pick and mix the software that align with their needs.

![Project 3D modules](./docs/Project3D_modules.png)

## Epics

### CTRL

- [CTRL Epic 01: Assign DUO Codes to Survey Questions](./CTRL_epics/CTRL01-duo_codes.md)
- [CTRL Epic 02: Import Participant List from REDCap](./CTRL_epics/CTRL02-redcap_participants.md)
- [CTRL Epic 03: Multiple Studies](./CTRL_epics/CTRL03-multi_study.md)
- [CTRL Epic 04: API Endpoints for ELSA Integration](./CTRL_epics/CTRL04-elsa_integration.md)
- [CTRL Epic 05: CTRL / ELSA Integration Automated Configuration](./CTRL_epics/CTRL05-ctrl_elsa_config.md)
- [CTRL Epic 06: Study Admin Role](./CTRL_epics/CTRL06-study_admin.md)
- [CTRL Epic 07: AAI solution integration for CTRL admin (AAF member)](./CTRL_epics/CTRL07-aai_integration_member.md)
- [CTRL Epic 08: AAI solution integration for CTRL admin (non-AAF member)](./CTRL_epics/CTRL07-aai_integration_non_member.md)

### REMS

- [REMS Epic 01: AAI solution integration](/REMS_epics/REMS01-aai_integration.md)

### Elsa

- [ELSA Epic 01: ELSA / REMS integration automated configuration](/ELSA_epics/ELSA01-rems_integration.md)
- [ELSA Epic 02: AAI solution integration](/ELSA_epics/ELSA02-aai_integration.md)
- [ELSA Epic 03: NCI Data Exchange of Full Dataset](/ELSA_epics/ELSA03-nci_data_exchange_full_dataset.md)
- [ELSA Epic 04: NCI Data Exchange of Predefined Subset](/ELSA_epics/ELSA04-nci_data_exchange_predefined_subset.md)
- [ELSA Epic 05: NCI Data Exchange of Sample Level Custom Subset](/ELSA_epics/ELSA05-nci_data_exchange_sample_subset.md)
- [ELSA Epic 06: NCI Data Exchange of File Level Custom Subset](/ELSA_epics/ELSA06-nci_data_exchange_file_subset.md)

### RDDP

- [RDDP Epic 01: Cohort-level beacon on RDDP datasets](/RDDP_epics/RDDP01-cohort_beacon.md)
