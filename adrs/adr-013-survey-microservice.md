# ADR 013: Survey Microservice

## Status

- 2024-09-24 Proposed
- 2024-09-26 Accepted

## Context

- There is a hard requirement to offer surveys to job candidates and employers.

## Decision

- We will implement a micro service to support the Survey MFE for managing surveys
- This will interface with the survey MFE (ADR-012) and the survey database (ADR-014)
- The service will not provide information on individuals' survey results, apart from indicating if the surveys have been offered or completed.

## Positive Consequences

- Standard microservice advantages (configuration, evolution, testability, etc).
- No need to update multiple applications if survey needs change

## Negative Consequences

- None

## Risks

- Potentially, having a single microservice for handling surveys might raise issues if the types and presentations of surveys are wildly different between different applications (i.e., if the surveys given to candidates and to employers have few/no similarities in data structure or question type). However, this is considered unlikely.
- It may be advisable to use a third-party survey tool to save money and developer time, in which case the MFE will function largely as a wrapper around it.
