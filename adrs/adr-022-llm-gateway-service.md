# ADR 022: LLM Gateway Service

## Status

- 2024-09-24 Proposed

## Context

- There are multiple hard requirements to use AI systems for resume and job processing.
- We are following a microservice architecture
- We want to avoid tying ourselves to a specific AI service or model

## Decision

- We will create an LLM Gateway Service
- All functionality that requires use of an LLM will use this service
- The LLM Gateway itself will not directly access LLMs, but will instead direct requests to an appropriate LLM microservice.
  - This will allow us to hide LLM functionality from the UI to prevent its abuse, and will also let us use an LLM-agnostic contract for the service calls
- Provided service: Gathering Employer Information
  - The system is expected to search the internet for available data on the organizations that post job openings.
  - This will return plain text information about the employer.

## Positive Consequences

- High degree of configurability and evolvability

## Negative Consequences

- Small performance hit from the pass-through
- Need to write multiple microservices for multiple LLMs.

## Risks

-
