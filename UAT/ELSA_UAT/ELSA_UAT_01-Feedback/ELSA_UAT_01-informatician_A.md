# UAT Report: ELSA UAT 01: Feedback

**Tester:** Informatician A

**Date:** 2026-05-19

**Environment:** uat

**Version:** 0.6.0

## Related GUARDIANS Task

3D-5-11: (Elsa) Conduct user acceptance testing to refine functionality and improve user experience.

## User Story

As a data custodian, I want to share a subset of a dataset stored on NCI with an authorised data requester, so that they can download data onto their authorized storage.

I should be able to:

- log onto Elsa data
- see the datasets that I am responsible for
- view the details of the datasets
- see data access requests approved by the data access committee.
- view details of the application regarding which data to be shared.
- verify consent of patients and data use statements.
- release data to the authorized data requester.

## Context

The comments below are based on the video recording of the demo of CTRL-Elsa-REMS-Sequera integration performed at the Biocommons in-person meeting 2025.

## Actions

### Else access

- Login using Auth0 / AAF
- Logout

### Dataset view

- See a list of datasets
- View the details of each dataset

### Release data

- Confirm that the DAC has approved the data access request
- Select the dataset to be given access
- Confirm that the data to be shared has got patient consent
- Select the patient data to be included in the release
  - Preference is to upload a CSV of all patient IDs as a way to select the patients because the dataset contains data from over 1000 patients (to be tested)
- Select the data types (e.g. bam, fastq, vcf, etc.)
- Configure how the data is to be accessed
- Enable the data sharing

## Feedback and issues

- It is unclear how the patient consent check can be done efficiently when there are over 1000 patients involved

> Elsa has two mechanism to check patient consent. i> static consent is recorded within Elsa database as part of the dataset registration process. ii> dynamic consent can be query at release creation through communication with CTRL, an e-consent platform. Feature yet to be tested at scale.

- Clicking the “Active Release” button will enable the sharing of the data and an email will be sent to the data requestors informing that the data is now available but I still need to manually configure how researchers are going to access the data

- Elsa UI display AWS, GCP and CloudFlare as supported storage location, none of this works with NCI where my dataset is hosted

- Elsa UI display various sharing mechanisms but there are all AWS infrastructure specific, none of this works with NCI (or GCP for that matter).
