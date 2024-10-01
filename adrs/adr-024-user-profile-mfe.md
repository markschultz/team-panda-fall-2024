# ADR 024: User Profile Micro Front End

## Status

- 2024-09-26 Proposed
- 2024-09-30 Accepted

## Context

- We are implementing a micro front end design for the UI (ADR-009)
- We need a way for users (employers and candidates) to create and manage their user profiles, including entering and updating their demographic information

## Decision

- We will implement a user profile MFE
- This will handle the UI portions of the following:
  - Creating logins
  - Updating/resetting passwords
  - Entering demographic details (optional, for reporting purposes)

## Positive Consequences

- Standard MFE positives (see ADR-009)

## Negative Consequences

- Standard MFE negatives (see ADR-009)
- The data will need to be synced to the analytics db (ADR-018) for reporting purposes

## Risks

- None
