# ADR 001: Main Architectural Characteristics

## Status

- 2024-09-23 Proposed
- 2024-09-24 Approved

## Context

- AI (and LLMs in particular) is a rapidly-evolving technology.
- In addition, the tech job space is routinely changing and adding new skills, languages, etc.
- Because of this, the expectation is that the system we build today may not be adequate, as-is, a few years from now. It will need to be able to be updated and/or reconfigured promptly and cost-effectively.

## Decision

- The key architectural characteristics we will be focused on are:
  - Scalability
  - Evolvability
  - Testability

- Secondary characteristics are
  - Fault-tolerance
  - Integration
  - Performance
  - Configurability

## Positive Consequences

- Focusing on evolvability will allow the system to change over time in response to new technology and shifting market conditions.
- Scalability will allow for spikes in needed capacity, as well as accommodate growth of use if the system proves popular.
- Testability is vital for any system that relies on LLMs. Regular validation of outputs is necessary

## Negative Consequences

- We are not considering cost or simplicity as key considerations. This could be an issue if the budget is tight.

## Risks

- Risks will be specific to the architecture that is chosen.
