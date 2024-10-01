# ADR 017: Blob Storage of Uploaded Files

## Status

- 2024-09-24 Proposed
- 2024-09-26 Accepted

## Context

- There is a requirement that we provide candidate resumes to employer users upon receipt of payment.
- Thus, we need to store uploaded resume files, including multiple versions

## Decision

- We will implement cloud file storage (e.g., AWS S3) for resume files.
- Information linking the uploaded files to specific users will be stored in the candidate database.

## Positive Consequences

- Flexible storage

## Negative Consequences

- A small monthly charge for file storage

## Risks

- None
