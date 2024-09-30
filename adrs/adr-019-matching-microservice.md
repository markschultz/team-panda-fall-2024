# ADR 019: Matching Microservice

## Status

- 2024-09-24 Proposed
- 2024-09-26 Accepted

## Context

- There is a hard requirement to find matches between candidates and jobs
- Resumes and job postings live in separate places (the candidate and employer microservices, specifically)

## Decision

- We will implement a matching service
- Included functionality:
  - Accepting (and storing) candidate matching data from candidates.
  - Accepting (and storing) job matching data from employers
  - Finding job matches for a candidate
  - Finding candidate matches for a job
- In order to support scalability, candidate matching data and job matching data will be queued initially, then processed at regular intervals.

## Positive Consequences

- Standard microservice advantages (configuration, evolution, testability, etc).
- We don't have to query across multiple services/businesses to find matches

## Negative Consequences

- If reporting is desired, data will have to be synced there


## Risks

- Need to guard against information becoming stale (e.g., if the user updates their resume, the candidate's new data will have to be passed to the matching service)-
