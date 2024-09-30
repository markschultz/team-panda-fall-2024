# ADR 007: Resume Microservice

## Status

- 2024-09-24 Proposed
- 2024-09-26 Accepted

## Context

- There is a hard requirement for candidates to be able to upload resumes, get tips on resumes, and search for job matches.
- There is a hard requirement for employers to be able to purchase resumes and then download them
- We have opted to implement micro front end UI and a microservices architectural style
- Our assumption is that when employers pay for access to a resume, they are paying for a resume and not for permanent access to the candidate's information

## Decision

- We will have a microservice for managing the following:
  - Resume uploads
    - This will interact with blob storage (ADR-017)
    - It will also interact with the LLM Gateway Service (ADR-022) to parse the resume and to extract its raw text
    - It will also interact with the LLM Gateway Service (ADR-022) to extract candidate metrics and submit them to the Matching Service (ADR-019)
  - Resume requests
    - Employers need to be able to submit requests to retrieve copies of a resume
  - Resume tips
    - This microserve will handle providing resume tips based on the extracted text of the resume.

## Positive Consequences

- Standard microservice advantages (configuration, evolution, testability, etc).
- Since we are passing the sanitized text of the resume instead of a database reference (when we extract metrics), we are not requiring the LLM service that handles the request to have any awareness of other services

## Negative Consequences

- Standard microservice disadvantages
- The data being passed in the call is potentially a few hundred KB, but this should still be not be a bandwidth concern.

## Risks

- We are making the assumption that employers have an established contractual relationship with ClearView that handles invoicing and billing.
