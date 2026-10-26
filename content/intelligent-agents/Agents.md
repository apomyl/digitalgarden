---
publish: true
aliases:
  - agent
created: 2026-10-17T09:23:57.151Z
modified: 2026-10-26T20:30:21.624Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> A software agent is defined below as a function and in words
>
> Let O be the set of observations and A the set of actions:
> $f : O^* \to A$
> $a_t = f(o_1, o_2, \dots, o_t)$
> _we use the observation history instead of the latest local observation because in a partially observable world, [[Perceptual Aliasing|one observation isn't enough to determine the true world state]]_
>
> ![[Is it an agent or just a program?#Definition]]

Definition/Feature breakdown:

- **Situated** - in an environment
- **Autonomous** - some action choices are its own
- **Goal-directed** - behaviour is evaluated relative to objectives
- **Persistent** - interaction typically unfolds over time

> [!tldr] Properties that we can have
> We assume agents are [[Rationality in agents|Rational]] not omniscient.
>
> Properties of an Intelligent Agent:
>
> - **[[Autonomous Agents|Autonomy]]** - controls aspects of its behaviour
> - **Reactivity** - responds to environmental changes in time
>   - _a [[Reactive Agent|reactive agent]]_ is an agent who relies solely on the latest observation
> - **Social ability** - interacts with other agents meaningfully (and humans)
> - **Proactivity** - takes initiative towards future objectives
>
> Social ability:
>
> - **[[Cooperation in Agent Systems]]** - working together as a team to achieve a shared goal
> - **[[Coordination in Agent Systems|Coordination]]** - managing the interdependencies between activites
> - **[[Negotiation]]** - the ability to reach agreements on matters of common interest
>
> Properties of the environment:
>
> - **Accessible** - agent has or can obtain complete, accurate, and up-to-date information about the state of the environment
> - **Static** - environment unchanged except by the actions of agent
> - **[[Probabilistic vs Deterministic|Deterministic]]** - actions have a single guaranteed effect, no uncertainty about result state
> - **Episodic** - current action does not affect subsequent action

> [!question] Agent Behaviour
>
> - How can we represent agent goals? - [[Model-based Agent]], [[Belief-Desire-Intention]]
> - What's a basic way an agent can determine how to act? - [[Sense-Decide-Act]]
> - Different types of agents? - [[Agent Architecture]]
> - How can we determine good behaviour? - [[PEAS]]

#### References

- [[Is it an agent or just a program?]]
