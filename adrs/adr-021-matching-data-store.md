# ADR 021: Matching Data Store

## Status

- 2024-09-24 Proposed
- 2024-09-30 Accepted

## Context

- There are hard requirements to find candidate/job matches using uploaded resume and job data
- For the best user experience, responses to requests for job matches should be synchronous and fast.

## Decision

- We will store candidate/job match results, candidate matching data, and job matching data in a data store
- The Employer Management and Candidate microservices will query this data store via the matching microservice (ADR-019) in order to retrieve match information.
- The matching microservice will queue candidate matching data and job matching data and process it periodically, so data will not be completely up-to-date.

## Positive Consequences

- Fast response to queries.

## Negative Consequences

- Matches will always be slightly stale (up to whatever the delay of the refresh is). However, given the time scale of a typical interview process it is not expected that delay of several minutes in finding out about a job or candidate will represent a problem.

## Risks

- Care needs to be taken to make sure that stale results get removed and no legitimate matches get missed.
