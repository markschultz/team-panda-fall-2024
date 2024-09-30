# ADR 026: User Profile Service

## Status

- 2024-09-26 Proposed
- 2024-09-30 Accepted

## Context

- We need a place for the profile microservice (ADR-025) to store user profile and demographic data

## Decision

- We will create a NoSql database to store user information documents containing their details and demographic data

## Positive Consequences

- Standard microservice advantages (configuration, evolution, testability, etc).

## Negative Consequences

- Standard microservice disadvantages
- The data will need to be synced to the analytics db (ADR-018) for reporting purposes

## Risks

- None (see ADR-026)
