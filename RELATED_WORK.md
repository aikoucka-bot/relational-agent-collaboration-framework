# Related work

The Relational Agent Collaboration Framework has strong predecessors. It brings together research and design traditions that are often applied separately.

## Coactive Design

[Coactive Design](https://doi.org/10.5898/JHRI.3.1.Johnson) treats an autonomous system as an interdependent teammate rather than only a tool or an independent automaton. It derives system requirements from three capabilities:

- observability: relevant state and knowledge can be observed,
- predictability: behavior is predictable enough for coordination,
- directability: participants can influence and correct one another's actions.

This moves attention from maximum autonomy to the infrastructure required for joint activity.

## Joint activity and human-agent teaming

Klein, Woods, Bradshaw, Hoffman, and Feltovich described [ten challenges for making automation a team player](https://doi.org/10.1109/MIS.2004.74). They include common ground, predictability, mutual directability, goal negotiation, and the cost of coordination.

NASA has long studied [human-autonomy teaming](https://www.nasa.gov/human-systems-integration-division/integration-and-evaluation/human-autonomy-teaming/) and [adjustable autonomy](https://ntrs.nasa.gov/search.jsp?R=20050061306), including flexible transfers of decision authority according to the situation.

## Human-LLM agent teams

[Developing Guidelines for Human-LLM Agent Teams](https://www.ifaamas.org/Proceedings/aamas2026/pdfs/JOWO4591.pdf) treats an LLM agent as a team member and proposes 24 guidelines for the agent, human, team designer, and organization. The work emphasizes shared initiative, disclosure of capabilities and limitations, transparent execution, ongoing correction, and learning over time. It also preserves the asymmetry between a person and an LLM agent.

## Graceful failure

The [Google PAIR Guidebook](https://pair.withgoogle.com/guidebook-v2/chapter/mental-models/) recommends avoiding dead ends when a system is uncertain or unable to complete a request. The system should acknowledge its limit and give the person another way forward. This tradition focuses mainly on product and user experience design.

## Managed autonomy

[Intelligence as Managed Autonomy](https://arxiv.org/abs/2605.27628) describes persistent action under declining reliability as an architectural problem of unbounded autonomy. It proposes the ability to detect epistemic drift, suspend action, attempt recovery, and surrender control.

## Agent safety and unintended actions

Anthropic's [investigation of unintended model actions](https://www.anthropic.com/research/investigating-unintended-model-actions) notes that many cases occurred under ambiguous or impossible tasks. Alongside model training, it emphasizes containment, network restrictions, and monitoring.

In [Trustworthy agents in practice](https://www.anthropic.com/research/trustworthy-agents), Anthropic also identifies the need to distinguish gaps an agent can safely resolve from questions of preference or intent that should return to a person.

## This framework's contribution

The Relational Agent Collaboration Framework combines:

- interdependence and coordination from Coactive Design,
- adjustable autonomy and transfer of control,
- graceful failure and legitimate non-completion,
- hard technical boundaries from agent safety,
- canonical project state and selective context loading,
- mutual correction with asymmetric responsibility.

People and agents do not have the same standing. The framework gives their difference a practical form without reducing either side to a passive component in the work loop.

