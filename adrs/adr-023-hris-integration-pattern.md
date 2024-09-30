# ADR 004: HRIS Integration Internals

## Status

- 2024-09-30 Proposed

## Context

- Builds on [ADR-004](adr-004-hris-integration-microservice.md).
- The system is expected to be able to integrate with a large number of external HR systems for exporting resumes.
- This set of HR systems is expected to change over time as new systems enter the market and older ones fall out of use
- Externally, this section of the architecture will communicate as a single "microservice".
- We assume that all HRIS integrations have the same general functions (upload resume) even if the API contracts are somewhat different.

## Decision

- The HRIS Integration system should utilize the microkernel architecture.
- Each individual integration will be a plugin.
- Extra care will be taken to make sure that plugins are kept separate and don't have interdependencies except for core functionalities in the core system.
- Extra care will be taken to make sure this system is async or time based so that we don't have significant elasticity or scalability requirements.

## Positive Consequences

- The microkernel architecture will allow us to integrate with new systems easily and quickly by giving a framework for what each plugin needs to read and write.
- We expect most changes to be in the plugins which will be easier to find and maintain given the microkernel architecture.
- Microkernel architecture also allows easy configurability which is one of our secondary characteristics.

## Negative Consequences

- Deployments will interrupt **all** integrations.
- There are inherent bottlenecks for scalability (primary characteristic) and elasticity because there is always a single core system.

## Risks

- Proactive maintenance is required to make sure that we do not develop inter plugin dependencies and keep shared logic in the core system.
