# ADR 008: Employer Information Microservice

## Status

- 2024-09-23 Proposed

## Context

- The system is expected to search the internet for available data on the organizations that post job openings.
- This information is used to help fill out details on the company and save effort by the users.


## Decision

- An Employer Information microservice should be created.
- The microservice should accept textual information about an employer as an input.
- The microservice should asynchronously use search engines to gather more information about the employer
- The microservice should call the LLM Gateway Service to get AI anlysis of the employer information
- Employer information (pre- and post-analysis) should be saved to a database (database type TBD)

## Positive Consequences

- Standard microservice advantages (configuration, evolution, testability, etc)

## Negative Consequences

- None

## Risks

- None
