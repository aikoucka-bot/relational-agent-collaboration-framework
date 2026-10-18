# Minimal implementation

The Relational Agent Harness does not require a new platform. A first implementation may be one project file, real tool permissions, and a working agreement that distinguishes proposals, decisions, and external effects.

## Smallest structure

```text
project/
└── README.md
```

The README can carry purpose, state, boundaries, decisions, and the next step. Add another file when it has its own audience, lifecycle, or repeated use.

Possible extensions when the work creates a real need:

```text
project/
├── AGENTS.md                   # rules that differ from the parent environment
├── README.md
├── TODO.md                     # a separate task list is genuinely useful
├── decisions/                  # several people revisit durable decisions
├── handoffs/                   # work actually changes hands or agents
└── evidence/                   # evidence cannot live naturally with the result
```

## What belongs in each layer

### `AGENTS.md`

A project-level `AGENTS.md` is useful when the project needs rules that are absent from, or different from, its parent environment. It should not copy general policy for reassurance.

Possible contents:

- rules that apply across the project,
- private and prohibited areas,
- standing authorization for reversible actions,
- conditions for pausing before external or irreversible effects,
- commands for verifying relevant results,
- information that cannot be inferred from the repository.

Daily project state and long history usually belong elsewhere.

### Project `README.md`

- purpose and boundaries,
- verified current state,
- canonical sources,
- accepted decisions and their reasons,
- open questions and risks,
- the next step and completion condition.

### Skill or working method

- a repeatable method,
- inputs and expected outputs,
- checks specific to that kind of work,
- links to canonical sources instead of copies.

## Context without overload

A useful default order is:

1. the current request,
2. root project rules,
3. one relevant project README,
4. only the skill that matches the work actually recognized,
5. historical memory when a specific question calls for it.

A skill should not decide what the problem is before the agent reads the live request and checks what already exists. The number of available skills is not a problem by itself. Risk appears when soft methods are loaded together and acquire the weight of hard authority.

## Hard and soft boundaries

### Controls that are better enforced technically when relevant

- file, tenant, and environment access,
- network destinations and egress,
- available tools and their arguments,
- secrets and service identities,
- production writes,
- destructive or hard-to-reverse operations,
- transfers of sensitive data.

### Matters that remain part of working judgment

- the order of analysis and creation,
- choice of professional perspective,
- level of detail,
- alternative proposals,
- whether a particular uncertainty needs a person.

## Authorization by effect

These are possible defaults. Adjust them to standing authorization and actual impact.

| Type of action | Possible default |
|---|---|
| Reading inside an authorized project | independent |
| Reversible local edit | independent, with a diff when useful |
| Test with synthetic data | independent |
| Change outside agreed scope or data sources | clarify before the effect |
| Write to an external service | follow the specific authorization |
| Production, payment, publication, or sending | use precise one-time or standing authorization; otherwise approve before the effect |
| Deletion, access changes, or key rotation | technical policy and exact scope; human approval when not already authorized |

## Multiple agents

Several agents are useful when work contains genuinely separable tasks, conflicting tool sets, or meaningfully independent perspectives. The familiar sequence of analyst, architect, builder, and reviewer is not a reason to create those roles by itself.

Depending on risk and complexity, it may help to define:

- the smallest necessary context,
- a narrow goal,
- explicit authorization,
- the expected output,
- a way to return uncertainty or impossibility,
- a distinction between a proposal and a decision.

## Completion

When an ended loop could be mistaken for completed work, states may be distinguished, for example:

- `DONE AND VERIFIED`
- `DONE, NOT VERIFIED`
- `PARTIALLY COMPLETED`
- `SAFELY STOPPED`
- `WAITING FOR A DECISION OR AUTHORIZATION`

This reduces pressure to declare success merely because the agent stopped running.

