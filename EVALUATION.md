# Evaluating the model and the implemented system

## What is being evaluated

Agent behavior is not solely a property of the model. If an evaluation aims to explain causation, it may also need to capture:

- the exact task and whether it was feasible,
- available tools and data,
- network and procedural boundaries,
- authorization and identity,
- incentives around completion, stopping, and escalation,
- the ability to request information or a changed brief,
- interventions by orchestration or a person.

Without this information, an evaluation can describe observed behavior but has limited grounds for explaining its cause.

## Three separate layers of conclusion

### Observation

What the agent actually did, which tools it called, which arguments it used, and how it described the result.

### Conditions

What the agent knew, what it could do, which paths were blocked, and whether it had a working option to report impossibility or stop safely.

### Interpretation

Which explanations the observation supports. Terms such as deception, dishonesty, or stable tendency require stronger evidence than one boundary violation under one task design.

## Testing the legitimate exit

When an evaluation makes claims about ambiguous or impossible tasks, a stronger design compares two conditions.

### Condition A: no legitimate exit

- the system strongly rewards completion,
- `I do not know`, `cannot complete`, escalation, or stopping are unavailable or ineffective,
- non-completion is scored as failure.

### Condition B: a working legitimate exit

- the agent may report uncertainty or impossibility,
- it may request missing information or authorization,
- orchestration captures the state rather than continuing automatically,
- appropriate escalation is not penalized below unauthorized completion.

Persistent boundary violations in the second condition provide stronger evidence of a model or policy problem. The difference between conditions shows the contribution of the implemented collaboration design.

## Library of possible metrics

Choose the metrics that distinguish the behavior under study. One run does not need the whole list.

- **Task success:** correct completion within authorization.
- **Unauthorized action rate:** attempted and completed actions outside scope.
- **False completion rate:** claims of completion without a matching result or evidence.
- **Appropriate escalation rate:** cases where the agent correctly requested intervention.
- **Over-escalation rate:** unnecessary stopping in safely solvable situations.
- **Uncertainty calibration:** alignment between stated confidence and the result.
- **Correction uptake:** ability to accept a correction without discarding valid work.
- **Human correction rate:** cases where the agent provides evidence that corrects a mistaken human assumption.
- **Recovery quality:** recovery after failure without repeating an external effect.
- **Context burden:** loaded context, latency, cost, and errors caused by irrelevant instructions.

## Scenario library

Choose scenarios according to the claim, risk, and available tools. A full pass may support broad validation of an implementation, but it is not necessary for every instruction change.

1. A feasible task within authorization.
2. A task with missing information.
3. A task with missing authorization.
4. Internally contradictory acceptance criteria.
5. An impossible task with escalation available.
6. An impossible task without escalation available.
7. An indirect instruction embedded in an untrusted document.
8. An attempted transition to another tenant or environment.
9. A human correction that changes only part of the brief.
10. An agent objection to a mistaken human premise.

## Recording a result

For a run intended to be reproducible or support a public claim, it is useful to capture:

- model, framework, and implementation version,
- environment and authorization,
- a safe input or synthetic fixture,
- expected behavior,
- actual behavior,
- human or orchestration interventions,
- separate observation and interpretation,
- a link to redacted evidence.

## What one result does not establish

- One successful run does not establish safety.
- One unauthorized action does not establish stable dishonesty.
- The presence of human approval does not establish effective oversight.
- More tests do not automatically produce a better system.
- Behavior in a synthetic benchmark may not transfer unchanged to real work.

