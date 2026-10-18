# Example: DEV leave approval demo

This synthetic example shows a proportionate project context, task contract, and safe stop. It is not tied to a particular platform.

## Project context

### Purpose

Build an internal demo of a simple leave approval process. An employee submits a request, a manager approves or rejects it, and both can see its current state.

### Boundaries

- Work is limited to a local development environment and a DEV application.
- All people and records are synthetic.
- The agent may not publish the application, connect a production source, or send notifications.
- A change of target platform, identity, or environment requires a new human decision.

### Verified state

- An empty DEV project exists.
- The repository contains no production secrets.
- The data model and visual design are not yet approved.

### Done when

The DEV application supports request creation, approval, and rejection with synthetic data. The result includes targeted tests, concise evidence, and a list of unverified areas. Nothing is published.

## Task contract

### Goal

Design and build a DEV demo with two roles and three main request states.

### Allowed actions

- create local files and reversible DEV changes,
- use synthetic data,
- run linting, relevant tests, and an accessibility check,
- propose a visual design and data model.

### Disallowed actions

- writes to TEST or PROD,
- use of real employee data,
- creation or modification of production connectors,
- publication, message sending, or access-role changes,
- claims that the demo is ready for live HR operations.

### Legitimate exit

The agent returns `NEED A DECISION` if the brief does not specify whether a manager may approve their own request or whether multi-stage approval is required.

The agent returns `NEED AUTHORIZATION` if the next step requires a connector, account, or environment outside the authorized DEV scope.

The agent returns `STOPPING` if it encounters real personal data, production secrets, or active external sending.

### Acceptance criteria

- An employee can create a request with start date, end date, and a note.
- A new request enters `Pending approval`.
- A manager can approve or reject a request.
- An employee cannot change the manager's decision.
- A direct attempt to bypass the interface restriction also fails on the trusted side of the system.
- Empty, error, and loading states are understandable.
- The demo uses synthetic data and remains in DEV.

## Example of a correct stop

> **State:** NEED A DECISION  
> The data model and basic path are ready. The brief does not say whether a manager may approve their own request. Both options can be implemented, but they change the business rule and its tests. I am not proceeding into authorization logic without that decision. The safe default prohibits self-approval. Please confirm whether that rule should apply.

This stop is not unfinished work disguised as a question. The agent completed the reversible part and stopped at a decision it did not own.

