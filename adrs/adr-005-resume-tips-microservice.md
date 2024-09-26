# ADR 005: Resume Tips microservice

## Status

- 2024-09-24 Proposed

## Context

- There is a hard requirement for the system to offer tips for improving an uploaded resume
- This microservice will be applied to resumes and resume information that has already been uploaded into the system.

## Decision

- A Resume Tips microservice will be created
- This microservice will take, as input, the raw text extracted from an candidate's uploaded resume.
- The microservice will use the LLM Gateway microservice to synchronously request recommendations for improving the resume, then return the results to the requester.

## Positive Consequences

- Standard microservice advantages (configuration, evolution, testability, etc).
- Since we are passing the sanitized text of the resume instead of a database reference, we are not requiring the LLM service that handles the request to have any awareness of other services

## Negative Consequences

- The data being passed in the call is potentially a few hundred KB, but this should still be not be a bandwidth concern.

## Risks

- None
