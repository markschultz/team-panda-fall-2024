# ADR 004: HRIS Integration Microservice

## Status

- 2024-09-24 Proposed
- 2024-09-26 Accepted

## Context

- The system is expected to be able to integrate with a large number of external HR systems for exporting resumes.
- This set of HR systems is expected to change over time as new systems enter the market and older ones fall out of use
- The specifics of the integration are not relevant to the primary mission of the system (matching candidates to jobs, and providing neutral summaries of resumes).

## Decision

- An HR integration microservice should be created.
- The specifics of the microservice (including its internal architecture) are outside the scope of this ADR.
- The HR Integration Microservice should accept references to uploaded resumes and deliver that resume to the specified HR system
- The HR Integration Microservice should accept the extracted plaintext version of a resume and deliver that resume to the specified HR system

## Positive Consequences

- The intergration with third-party HR systems can be isolated from the rest of the system, essentially becoming a black box that outputs jobs and accepts resume data as inputs.

## Negative Consequences

- None

## Risks

- This is not a risk for the microservice specifically, but any means of integrating with external HR systems will require some level of dedicated maintenance to keep it up to date.
