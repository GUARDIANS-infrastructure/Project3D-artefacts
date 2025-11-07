# ELSA Epic 03: NCI Data Exchange of Full Dataset

## Related GUARDIANS Task

3D-4-7: (Sharing) Defined core use-cases, requirements, acceptance criteria, and stub integration tests for APIs providing secure access to data, ensuring compliance with open standards (for example these may include GA4GH passports, DRS, htsget), available on a platform like GitHub.

## User Story

As a data steward, I want to share an entire dataset stored on NCI with an authorised researcher, so that they can download data onto their authorized storage.

## Context

- Researcher has file a Data Access Request to the dataset (through REMS)
- Data Access Request has been approved by the Data Access Committee (through REMS)
- Dataset is stored on NCI
- Dataset is registred in Elsa

## Acceptance Criteria

- [ ] The researcher can be identified across REMS, Elsa and NCI, confirming it is the same individual.
- [ ] If the researcher is authorized to download the dataset directly:
  - [ ] the data steward can programmatically grant the researcher access to the dataset stored on NCI using Elsa.
  - [ ] the researcher can then read and/or download the data.
- [ ] If the researcher is authorized to transfer the data in a dedicated storage only:
  - [ ] the data steward can programmatically initiate the transfer of the dataset stored on NCI using Elsa to the dedicated storage.
  - [ ] the researcher can then read the data.

