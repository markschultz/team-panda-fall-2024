# ADR 012: Survey Micro Front End

## Status

- 2024-09-24 Proposed

## Context

- We are implementing a micro front end design for the UI (ADR-009)
- There is a hard requirement to offer surveys to job candidates and employers.
- We need to provide a user interface for creating and administering those surveys.

## Decision

- We will implement a Survey MFE
- This will handle the UI portions of the following:
  - Creating candidate surveys
  - Creating employer surveys
  - Managing surveys

## Positive Consequences

- Standard MFE positives (see ADR-009)

## Negative Consequences

- Standard MFE negatives (see ADR-009)

## Risks

- Surveys are potentially complex. It may be advisable to use a third-party survey tool, which could affect implementation of the survey MFE.
