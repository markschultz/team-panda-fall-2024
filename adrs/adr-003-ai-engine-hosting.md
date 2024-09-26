# ADR 003: AI Engine Hosting

## Status

- 2024-09-22 Proposed

## Context

- We expect to make heavy use of multiple LLMs (for parsing resumes, parsing job requirements, and generating descriptions of candidates).
- We further expect to use specialized LLMs for the above.
- SaaS LLMs are extremely expensive to use
- AI usage will need to ramp up and down quickly in response to user demand
- We need high transparency and testability for the LLMs in order to measure quality of output.

## Decision

- We will host our own AI systems in a cloud environment.

## Positive Consequences

- In the mid to long term this will be cheaper than SaaS.
- In both the short and long term this is cheaper than self-hosting on our own hardware.
- This also gives us the best testability options, since we control the data and the servers and can spin up testing machines as needed.
- Since we have full control of the LLM, we can control when it is updated and monitor what changes are made. This will prevent unpredictable changes in output that might otherwise happen if we were dependent on a third-party server.

## Negative Consequences

- This will require more setup time during the initial project, since we can't just plug-and-play ChatGPT or some other system.
- This will also require us to train our own models, both initially and as the market changes.

## Risks

- Finding specialized expertise in creation and training of LLMs can be difficult, as the skillset is currently in very high demand.
