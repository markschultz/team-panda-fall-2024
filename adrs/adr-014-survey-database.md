# ADR 014: Survey Database

## Status

- 2024-09-24 Proposed

## Context

- There is a hard requirement to offer surveys to job candidates and employers.
- A place is needed to store both the surveys and the individual responses to survey questions
- The content  of the surveys will change dynamically over time
- Reporting will not be done against this database, apart from checking the status of individual surveys

## Decision

- We will use a cloud-hosted NoSql database
- For reporting, surveys and survey results will be imported to the analytics database (ADR-018).
- No PII should be stored in this database, apart from the user ID of the user who answered the survey.

## Positive Consequences

- No need to commit to particular data structures for the surveys

## Negative Consequences

- We are effectively ruling out doing large-scale reporting directly against this database.

## Risks

-
