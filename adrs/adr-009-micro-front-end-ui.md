# ADR 009: Use of "Micro Front End" design

## Status

- 2024-09-24 Proposed

## Context

- Several user interfaces are needed for the system (candidates, surveys, employers, administrators).
- With the exception of administration, none of the user interfaces requires knowledge of the others

## Decision

- We will implement a "micro front end" design.
- This includes having a primary "framework" UI into which the candidate, survey, employer, and administrator UIs are fit
- The framework UI will include the following:
  - Navigation bars
  - Login/authorization screens

## Positive Consequences

- Separate development of the different UIs will be easier

## Negative Consequences

- Making the UI less monolithic has some of the same downsides as making the back end non-monolithic. Up-front design is more complicated and has higher cost.
-

## Risks

-
