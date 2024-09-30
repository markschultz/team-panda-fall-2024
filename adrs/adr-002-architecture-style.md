# ADR 002: Architectural Style

## Status

- 2024-09-23 Proposed
- 2024-09-25 Accepted

## Context

- Per ADR-001, the architecture will focus on configurability, evolvability, and testability.
- Cost and simplicity will not be major considerations

## Decision

- We will be using the Microservices architectural style for the overall project.

## Positive Consequences

- Per the architecture styles worksheets, microservices easily beat alternatives in the three main areas of consideration (13 stars versus 10 for the next-best)
- Microservices supports configurability well because the HR integration module and the LLM module are independent services, meaning configuration changes to one system can be performed in isolation from others
- Testability is easier in a microservices architecture because, again, each component of the system can be tested in isolation.
- Evolvability is the area where microservices shine the most. Each microservice can be altered, or even replaced with a new system altogether, without impacting other systems, provided existing contracts are honored.

## Negative Consequences

- A microservice architecture scores poorly for cost. However, it is our experience that this is only true in the short-term. In the longer term, the higher configurability, evolvability and testability of a microservices architecture makes projects that use it cheaper and faster to develop for.
- A microservices architecture starts off more complicated than other styles (monolith in particular). This requires additional up-front planning about areas of responsibility and data ownership.

## Risks

- This is a higher-cost option, in the short term.
