# ADR 025: User Profile Service

## Status

- 2024-09-26 Proposed
- 2024-09-30 Accepted

## Context

- We are implementing a microservice architectural style (ADR-002)
- We need a way for users (employers and candidates) to create and manage their user profiles, including entering and updating their demographic information

## Decision

- We will have a microservice for managing the following:
  - Creating logins
  - Resetting passwords
  - CRUD operations on personal and demographic data for users

## Positive Consequences

- Standard microservice advantages (configuration, evolution, testability, etc).

## Negative Consequences

- Standard microservice disadvantages
- The data will need to be synced to the analytics db (ADR-018) for reporting purposes

## Risks

- None (see ADR-026)
