# ADR 020: Data Aggregator

## Status

- 2024-09-24 Proposed
- 2024-09-30 Accepted

## Context

- The primary sources of data we need to report on are located in multiple databases.
- A decision has been made to have an analytics database where data is consolidated for reporting purposes.

## Decision

- We will create a data aggregation process to copy data from source databases to the reporting and analytics database
- We will use change data capture from the source databases and a stream processing framework in the data aggregator
- There are a lot of TBD implementation details here

## Positive Consequences

- Allows the analytics database to exist (ADR-018)
- Change data capture allows analytics data to be captured automatically without affecting source database performance

## Negative Consequences

- The need for an aggregator is itself a negative consequence of ADR-018.
- Joining and aggregation of multiple separate but related data streams can be complex, but the use of a stream processing framework makes common tasks such as joins more feasible.
- Change data capture involves tight coupling to the models in the source database, so significant model changes may require changes in the data aggregation service.

## Risks

- Need to guard against data corruption during the sync process
