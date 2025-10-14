# CTRL Epic 04: CTRL / ELSA integration automated configuration

## Related GUARDIANS Task

3D-4-1: Demonstrated implementation of integration with upstream provider of consent status (REDCap) and downstream consumer of consent status via successful integration tests; released on a platform like GitHub with documentation and an open-source license.

## User Story

As a sys admin, I want to deploy CTRL and ELSA using infrastructure as a code, so that necessary accounts, API keys and URL endpoints required for intagration are automatically configured.

## Context

## Acceptance Criteria

- When CTRL and Elsa are deployed together, via infrastructure as code, a CTRL API key is automatically generated
- Elsa is automatically configured with the CTRL API endpoint and API key.
