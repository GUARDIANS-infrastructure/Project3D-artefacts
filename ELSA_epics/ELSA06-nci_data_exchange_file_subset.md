# ELSA Epic 06: NCI Data Exchange of File Level Custom Subset

## Related GUARDIANS Task

3D-4-7: (Sharing) Defined core use-cases, requirements, acceptance criteria, and stub integration tests for APIs providing secure access to data, ensuring compliance with open standards (for example these may include GA4GH passports, DRS, htsget), available on a platform like GitHub.

## User Story

As a data steward, I want to share a custom subset of a dataset stored on NCI with an authorised researcher, so that they can download data onto their authorized storage.

## Context

- Researcher has file a data access request for the dataset (through REMS)
- Data access request has been approved by the data access committee (through REMS)
- Dataset is stored on NCI
- Dataset is registred in Elsa data
- Custom subset is derived from data access request and sample information
- Custom subset granularity is done at a sample level and file level
  - Example: MGRB dataset: VCF of Female above 45 years old
  - Example: MGRB dataset: CRAM of European ancestry with blood glucose measurement

## Acceptance Criteria

- [ ] The researcher can be identified across REMS, Elsa and NCI, confirming it is the same individual.
- [ ] If the researcher is authorized to download the subset directly:
  - [ ] the data steward can programmatically grant the researcher access to the custom subset stored on NCI using Elsa.
  - [ ] the researcher can then read and/or download the data.
- [ ] If the researcher is authorized to transfer the data in a dedicated storage only:
  - [ ] the data steward can programmatically initiate the transfer of the custom subset stored on NCI using Elsa to the dedicated storage.
  - [ ] the researcher can then read the data from the dedicated storage.
