# ADR 018: Analytics database

## Status

- 2024-09-24 Proposed
- 2024-09-26 Accepted

## Context

- We need to be able to generate reports on candidates, jobs, and matches in order to check for bias and other undesirable results
- The primary sources of all of the data we need to report on are located in other databases (ADR-008, ADR-016, ADR-019)

## Decision

- We will create a SQL database for analytics
- This database will be populated by the data aggregator (ADR-020)

## Positive Consequences

- Will allow for easy creation of reports
- Fast response times since we are not aggregating data from multiple sources at time of report

## Negative Consequences

- The need to sync the data (and keep in in sync). See ADR-020

## Risks

- As with any project that involves syncing and reporting on data, care will have to be taken that stale or inaccurate data is kept out of the database.
