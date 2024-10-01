# ADR 022: LLM Gateway Service

## Status

- 2024-09-24 Proposed
- 2024-09-30 Accepted

## Context

- There are multiple hard requirements to use AI systems for resume and job processing.
- We are following a microservice architecture
- We want to avoid tying ourselves to a specific AI service or model
- Different LLMs potentially have different strengths and weaknesses

## Decision

- We will create an LLM Gateway Service
- All functionality that requires use of an LLM will use this service

- The LLM Gateway itself will not directly access LLMs, but will instead direct requests to an appropriate LLM microservice.
  - This will allow us to hide LLM functionality from the UI to prevent its abuse, and will also let us use an LLM-agnostic contract for the service calls
- Endpoints provided by the gateway (but provided by one or more microservices behind it) will include:
  - Gathering Employer Information
    - The system is expected to search the internet for available data on the organizations that post job openings. This search is part of this endpoint.
      - The reasoning here: some LLMs will perform such searches when prompted. Since such searches are part of the requirements (when retrieving employer data), it makes sense to move such searches behind the gateway. Either the LLM will do the search, or a dirrent service will do it and feed the results to the LLM.
  - Parsing skill/history/education/goal data out of resumes
  - Extracting raw text from resumes
  - Providing tips for improving resumes
  - Parsing skill/history/education requirments out of job offers
  - Scrubbing PII and potentially bias-related data from resumes
- Most endpoints should follow a strict contract of allowed parameters/properties rather than directly exposing the LLM prompt
  - The one possible exception to this is the resume tips endpoint. Depending on implementation, we may want to allow a move "conversational" approach to the user.
  - Another possibility is that we may want to prompt users and let them provide more goal information, if their resume lacks it, in order to help with collection of S.M.A.R.T. data.

## Positive Consequences

- High degree of configurability and evolvability
- This allows most the rest of the system to remain agnostic not only about what what specific LLMs are being used, but also about whether or not LLMs are used at all.
  - For example, if a third-party provider should happen to come along that already has an excellent system for extracting raw text and scrubbing PII, that could be plugged in behind the gateway without the front end or other services needing to know

## Negative Consequences

- Small performance hit from the pass-through
- Need to write multiple microservices for multiple LLMs.

## Risks

- There are no apparent risks apart from those inherent to using LLMs.
