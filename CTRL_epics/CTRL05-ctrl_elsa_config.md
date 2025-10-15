# CTRL Epic 05: CTRL / ELSA integration automated configuration

## Related GUARDIANS Task

3D-4-1: Demonstrated implementation of integration with upstream provider of consent status (REDCap) and downstream consumer of consent status via successful integration tests; released on a platform like GitHub with documentation and an open-source license.

## User Story

As a sys admin, I want to deploy CTRL and ELSA using infrastructure as a code, so that necessary accounts, API keys and URL endpoints required for intagration are automatically configured.

## Context

![Elsa context diagram](../docs/CTRL04-elsa_context_diagram.svg)
source: [Elsa](https://github.com/elsa-data/elsa-data/blob/dev/docs/architecture/context.drawio.svg)

## Acceptance Criteria

- An API endpoint that takes a list of participant IDs and returns corresponding DUO codes
- CTRL participants should have a unique identifier that match the records in Elsa
