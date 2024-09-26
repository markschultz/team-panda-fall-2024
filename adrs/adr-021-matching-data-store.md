# ADR 021: Matching Data Store

## Status

- 2024-09-24 Proposed

## Context

- There are hard requirements to find candidate/job matches using uploaded resume and job data
- For the best user experience, responses to requests for job matches should be synchronous and fast.

## Decision

- We will store candidate/job match results in a data store
- Another service (TBD) will refresh the store at regular intervals (several minutes).
- The Employer Management and Candidate microservices will query this data store in order to retrieve match information
  - Should there be a microservice for this?

## Positive Consequences

- Fast response to queries.

## Negative Consequences

- Matches will always be slightly stale (up to whatever the delay of the refresh is). However, given the time scale of a typical interview process it is not expected that delay of several minutes in finding out about a job or candidate will represent a problem.

## Risks

- Care needs to be taken to make sure that stale results get removed and no legitimate matches get missed.
