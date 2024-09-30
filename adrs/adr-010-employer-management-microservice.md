# ADR 010: Employer-management-microservice

## Status

- 2024-09-24 Proposed
- 2024-09-26 Accepted

## Context

- We are following a microservice architectural style
- There is a hard requirement for employer representatives to be able to manage information about the employer
- There is a hard requirement for employers to be able to input new job postings
- There is also a hard requirement for employer representatives to be able to search for matches on a job posting, and to review candidates.

## Decision

- We will implement an Employer Management microservice
- This microservice will support the following:
  - Adding/editing details about the employer
  - Adding/editing job postings

## Positive Consequences

- Standard microservice advantages (configuration, evolution, testability, etc).

## Negative Consequences

-

## Risks

-
