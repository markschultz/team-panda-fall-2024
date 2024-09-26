# ADR 015: Candidate Microservice

## Status

- 2024-09-24 Proposed

## Context

- There is a hard requirement for candidates to be able to upload resumes, get tips on resumes, and search for job matches.
- We have opted to implement micro front end UI and a microservices architectural style

## Decision

- We will have a microservice for managing the following:
  - Resume uploads
    - This will interact with blob storage (ADR-017)
    - It will also interact with the LLM Gateway Service (ADR-022) to parse the resume and to extract its raw text
  - Searches for job matches
    - This passes through to the matching service (ADR-021)

## Positive Consequences

- Standard microservice advantages (configuration, evolution, testability, etc).

## Negative Consequences

- None

## Risks

-
