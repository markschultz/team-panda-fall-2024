# ADR 016: Candidate database

## Status

- 2024-09-24 Proposed

## Context

- Candidates will be updating resumes, which will in turn be parsed to extract metrics and raw text
- We are following a microservice architecture, which implies a dedicated database for each microservice

## Decision

- We will use a NoSql database for storing candidate information
- This does not include storing the actual resume file. That will be stored in the blob stotage (ADR-017). A reference to it should be stored in the candidate document
- Information about candidate-job matches is not stored here. It is stored in the matching data store (ADR-021)

## Positive Consequences

- Ease of use
- No need to commit to a single data model for candidates/documents in advance.

## Negative Consequences

- We are effectively ruling out doing large-scale reporting directly against this database.

## Risks

-
