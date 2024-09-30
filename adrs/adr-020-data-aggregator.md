# ADR 020: Data Aggregator

## Status

- 2024-09-24 Proposed
- 2024-09-30 Accepted

## Context

- The primary sources of data we need to report on are located in multiple databases.
- A decision has been made to have an analytics database where data is consolidated for reporting purposes.

## Decision

- We will create a data aggregation process to copy data from source databases to the reporting and analytics database
- There are a lot of TBD implementation details here

## Positive Consequences

- Allows the analytics database to exist (ADR-018)

## Negative Consequences

- The need for an aggregator is itself a negative consequence of ADR-018. The aggregator itself has no negatives.

## Risks

- Need to guard against data corruption during the sync process
