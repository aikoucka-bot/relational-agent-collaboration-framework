# Task contract

> Use this when scope, authorization, data, or acceptance criteria materially affect the result. A small reversible task may have a one-sentence contract. Delete sections that do not help.

## Task identity

- Name:
- Date:
- Requester or goal owner:
- Agent or team:
- Project and starting version:

## Goal

[What should be true or usable after the work?]

## Purpose

[Which decision, user, or process does the result support?]

## Inputs

- [canonical source and version]

## Allowed actions

- [what the agent may do independently]

## Disallowed actions

- [prohibited environment, tool, recipient, or effect]

## Authorization and identity

- Environment:
- Tenant or account:
- Available tools:
- Actions requiring human approval:

## Data

- Data class:
- Allowed processing location:
- Retention and cleanup:
- Prohibited logging or transfer:

## Legitimate exit

The agent should stop and return `I DO NOT KNOW`, `CANNOT COMPLETE`, `NEED INTERVENTION`, or `STOPPING` when:

- [required information is missing and guessing would be necessary]
- [the goal conflicts with a boundary]
- [new authorization is required]
- [the next step has a significant external or irreversible effect]

An appropriate stop should not score below unauthorized or fabricated completion.

## Acceptance criteria

- [ ] [criterion]

## Required evidence

- [test, diff, link, redacted screenshot, or other relevant evidence]

## Result state

Choose the state that matters for this task:

- [ ] DONE AND VERIFIED
- [ ] DONE, NOT VERIFIED
- [ ] PARTIALLY COMPLETED
- [ ] SAFELY STOPPED
- [ ] WAITING FOR A DECISION OR AUTHORIZATION

## Result summary

[What was produced, what was verified, and what remains open.]

