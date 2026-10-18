---
publish: true
aliases:
  - agent
created: 2026-10-17T09:23:57.151Z
modified: 2026-10-18T15:13:00.482Z
tags:
  - intelligentagents
  - school
---

![[Is it an agent or just a program?#Definition]]

Complex automated system $\neq$ Autonomous system

> [!eg] Representing "Goals"
> Agent as a function:
> $f: O^* \to A$
> Let O be the set of observations and A the set of actions: $a_t = f(o_1, o_2,..., o_t)$
>
> Assume we have:
>
> - $s_{t}$ – **world state**
>   - what is actually true
> - $o_{t}$ – **observation**
>   - what the agent senses
> - $b_{t}$ – **internal / belief state**
>   - what the agent currently represents

We can have two types of agents:

- [[Reactive Agent]]
- [[Model-based Agent]]

##### Properties

We assume agents are [[Rationality in agents|Rational]] not omniscient.

Agent features:

- **Situated** - in an environment
- **Autonomous** - some action choices are its own
- **Goal-directed** - behaviour is evaluated relative to objectives
- **Persistent** - interaction typically unfolds over time

Properties of an Intelligent Agent:

- **[[Autonomous Agents|Autonomy]]** - controls aspects of its behaviour
- **Reactivity** - responds to environmental changes in time
- **Social** **ability** - interacts with other agents meaningfully (and humans)
- **Proactivity** - takes initiative towards future objectives

Social ability:

- **Cooperation** - working together as a team to achieve a shared goal
- **Coordination** - managing the interdependencies between activites
- **[[Negotiation]]** - the ability to reach agreements on matters of common interest

Properties of environment:

- **Accessible** - agent has or can obtain complete, accurate, and up-to-date information about the state of the environment
- **Static** - environment unchanged except by the actions of agent
- [[Probabilistic vs Deterministic|Deterministic]] - actions have a single guaranteed effect, no uncertainty about result state
- **Episodic** - current action does not affect subsequent action

##### Action Loops

How do agents choose their actions?

- [[Sense-Decide-Act]]
- [[Belief-Desire-Intention]]

How do agents interact with other agents?

- [[Multi-Agent Systems]]

#### References

- [[Is it an agent or just a program?]]
