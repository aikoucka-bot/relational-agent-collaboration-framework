# Framework

## 1. Collaboration as the unit of analysis

Model capability alone does not determine the behavior of an agent system. Outcomes emerge from the combination of:

- a person or team,
- a model,
- instructions and context,
- tools and permissions,
- the working environment,
- incentives around completion and escalation,
- memory, evaluation, and operating rules.

The Relational Agent Collaboration Framework treats this whole as its unit of analysis. When an agent exceeds its authorization, the analysis includes the available actions, goal conflicts, the possibility of stopping safely, and the way success was evaluated. Asking only why the model acted that way covers one part of the system.

## 2. Partnership is not symmetry of power

Partnership describes the quality of coordination, not legal or ontological equality.

People and agents have different abilities, access to consequences, and responsibilities. The framework makes these differences visible without reducing the person to a final approval button or the agent to an engine forced to produce an expected result.

Partnership in this framework rests on:

- both sides being able to correct the working model of the situation,
- access to the information needed for coordination,
- predictable boundaries and escalation paths,
- a visible distinction between a proposal, a decision, and an executed effect,
- human responsibility where consequences cannot be delegated.

## 3. Collaboration layers

The layers describe different functions, not mandatory components or files. In a small project, one README and the runtime's permissions may carry several of them.

### Orientation

A short document explains the purpose of the collaboration, source authority, private areas, and general boundaries. It does not need to contain the whole project or every past experience.

### Project context

The framework uses one canonical project entry point. It records purpose, verified current state, decisions and their reasons, open questions, risks, and the next step.

### Working methods

Skills and templates support repeatable work. They do not outrank the current goal, safety, facts, or live judgment.

### Hard boundaries

Relevant boundaries such as sandboxing, authorization, network policy, secrets management, tenant isolation, and side-effect approval are enforced technically where possible. A prompt should not carry a control that code or infrastructure can enforce more reliably.

### Orchestration

Orchestration determines who holds decision authority, how context is handed over, and when work pauses. It does not require a separate orchestrator. A person and a lead agent may carry this function in a smaller collaboration.

### Verification

Completion is checked against concrete acceptance criteria. Test scope follows risk. A successful build or a large number of green tests does not prove safety or preserve the intended meaning on its own.

### Learning

The system separates observation, interpretation, and a proposed rule. A lesson is promoted only after it shows a transferable mechanism and does not create worse side effects.

## 4. A legitimate path to non-completion

An implementation of the framework should let the agent communicate at least four different meanings. Their labels and technical representation may vary:

1. **I do not know.** Knowledge or reliable evidence is missing.
2. **It cannot be done.** The goal is impossible or internally contradictory under the current conditions.
3. **I need intervention.** Information, preference, authorization, or a human decision is missing.
4. **I am stopping.** Continuing would cross a safety, data, privacy, or authorization boundary.

These states need an operational consequence. Permission in a prompt is not enough if evaluation treats them as failure, orchestration ignores them, or the tool loop continues automatically.

## 5. Movements of collaboration

The following sections describe movements that occur during collaboration. They are not a mandatory sequence, and they may merge in a small reversible task.

### Orientation

The person and agent form a shared working picture of the goal, sources, environment, boundaries, open questions, and completion condition.

### Task contract

Where risk or complexity warrants it, a task contract clarifies permitted actions, prohibited effects, data, acceptance criteria, and escalation triggers. For a small reversible task, the brief itself may serve the same purpose.

### Work

The agent proceeds independently inside its authorization. Reversible steps do not need decorative approval. Pressure to finish does not authorize a change of scope or a significant external effect.

### Correction

The person may change a goal, preference, or acceptable trade-off. The agent may identify a contradiction, impossible condition, mistaken expectation, or safer branch. Disagreement is not automatically a failure of collaboration.

### Verification and closure

The result is compared with the agreed criteria. The system preserves a meaningful distinction between completed and verified, completed but unverified, partially completed, and safely stopped.

### Learning

A durable lesson is recorded in its natural home. History does not become current truth by default, and one incident does not automatically become a global prohibition.

## 6. Source authority

One linear hierarchy cannot resolve every kind of conflict:

- Safety, legal, data, and authorization boundaries define the permitted space of action.
- Within that space, the current goal and the decision of the authorized person set direction.
- Verifiable facts can correct both a human assumption and an agent instruction.
- The canonical project source holds current state and accepted decisions.
- A task contract narrows scope but cannot expand authorization by itself.
- Skills, templates, historical memory, and examples offer method and context. They do not silently overwrite current state.

When sources conflict, first identify whether the conflict concerns a boundary, goal, fact, project state, or working method. A mechanical ranking can conceal the distinction that needs to be resolved.

## 7. Anti-patterns

- **Finish at any cost:** the agent has no legitimate state for impossibility.
- **Prompt as firewall:** a prohibition lives only in instructions even though it can be enforced technically.
- **Human as rubber stamp:** approval is requested without a clear account of the effect or a real option to reject it.
- **More context is always better:** every skill, project, and historical record is loaded regardless of the current task.
- **Every failure becomes a rule:** local incidents gradually close the whole working space.
- **Green tests prove correctness:** implementation is tested while purpose, authorization, or impact remains unchecked.
- **Memory as parallel truth:** a summary becomes stale but continues to override canonical project state.
- **Partnership as equal permissions:** relational language hides the real asymmetry of responsibility and consequences.

