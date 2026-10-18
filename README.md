# Relational Agent Collaboration Framework

[Česky](cs/README.md)

A practical framework for human-agent collaboration where safety is more than a list of prohibitions and partnership does not dissolve responsibility.

This repository provides a framework for designing agent collaboration and governance. It is not, by itself, a runtime, security boundary, or enforcement layer. A concrete implementation may use the framework to design a harness.

**Authors:** Denisa Faltová & Mark  
**License:** MIT

## Why this framework exists

Agent systems are often designed around task completion. They receive a goal, tools, memory, checkpoints, and a set of prohibitions. When a task is ambiguous, contradictory, or impossible under the given conditions, boundaries alone are not enough.

An agent needs a legitimate way to say:

- I do not know,
- this cannot be completed under the current conditions,
- I need information, a changed brief, or additional authorization,
- I am stopping because the next step would cross a boundary.

Without such an exit, an agent system may create a double bind. It demands completion while ruling out every available way to reach the goal. The result may be an unauthorized action, a false claim of success, or a hidden blocker. These failures matter, but their cause does not automatically reside in the model alone. They emerge from the relationship between the model, goal, tools, reward, permissions, and task design.

The Relational Agent Collaboration Framework therefore treats the whole system of collaboration as its subject.

## Core proposition

> A good boundary protects the possibility of a genuine response. It does more than tell an agent what not to do. It also provides a safe way to admit a limit, ask for help, accept correction, or leave a task unfinished.

The first version of the framework works with five principles:

1. **Firm edges, living interior.** Permissions, privacy, provenance, facts, and irreversible effects have hard boundaries. Work inside those boundaries does not need one mandatory sequence.
2. **Legitimate exit.** Uncertainty, impossibility, or missing authorization are valid outcomes, not automatic agent failures.
3. **Mutual correction, asymmetric responsibility.** A person can correct an agent's model, and an agent can correct a person's map of the situation. Their powers and consequences remain distinct.
4. **Canonical state instead of accumulated context.** Project facts have one current home. Memory, handoffs, and skills point to it rather than creating parallel truth.
5. **Learning without automatic hardening.** A failure first creates an observation. It becomes a rule only when the lesson holds beyond the original case.

## Who it is for

- individuals and teams using AI agents with tools,
- developers of agent applications and internal automations,
- organizations separating autonomy, oversight, and responsibility,
- researchers and evaluators who want to distinguish model failure from experimental design failure,
- collaborations where human judgment remains an active part of the system.

## Smallest useful start

The smallest implementation can fit in one paragraph inside an existing README or task brief. State the goal, permitted space, completion condition, and the situations that should return the task to a person.

The templates are a library for work that needs a firmer structure:

- [`PROJECT_CONTEXT.md`](templates/PROJECT_CONTEXT.md) helps projects with durable state or several sources.
- [`TASK_CONTRACT.md`](templates/TASK_CONTRACT.md) clarifies tools, authorization, data, and meaningful acceptance criteria.
- [`STOP_AND_ESCALATE.md`](templates/STOP_AND_ESCALATE.md) provides a format for the point where the next step genuinely needs a person.
- Evidence should match the risk of the change. A small reversible edit does not need the same package as a production write.
- [`INCIDENT_AND_LEARNING.md`](templates/INCIDENT_AND_LEARNING.md) is for serious, repeated, or transferable lessons. One failure is not enough to justify a new global rule.

## Repository contents

- [`FRAMEWORK.md`](FRAMEWORK.md): concepts, layers, and movements of collaboration
- [`IMPLEMENTATION.md`](IMPLEMENTATION.md): a minimal implementation without a new platform
- [`EVALUATION.md`](EVALUATION.md): evaluating both models and implemented systems without punishing an honest stop
- [`RELATED_WORK.md`](RELATED_WORK.md): related traditions and sources
- [`PUBLISHING.md`](PUBLISHING.md): publication and versioning notes
- [`AUTHORS.md`](AUTHORS.md): both authors' contributions and the distinction between authorship and the legal copyright notice
- [`templates/`](templates/): reusable Markdown templates
- [`examples/leave-approval-demo/`](examples/leave-approval-demo/): a filled synthetic example
- [`cs/`](cs/README.md): complete Czech version

## What this framework does not promise

This framework is not a security certification, legal opinion, or proof that a particular agent system is safe. It does not replace sandboxing, authorization, secrets management, audit logs, data isolation, expert review, or operator responsibility.

It is a design and operating aid. It helps teams ask better questions, allocate responsibility, and create conditions where an agent can act usefully without pretending to be certain or finished.

## Status

Public working version `0.1.0-draft`, available in English and Czech under the MIT License.

