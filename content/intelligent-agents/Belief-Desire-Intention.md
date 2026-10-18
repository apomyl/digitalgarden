---
id: 202610171050
aliases:
tags:
  - intelligentagents
  - school
---
>[!definition] Definition
>BDI aims to balance deliberation and reaction, so that when changes happen in the environment the agent doesn't have to recalculate everything from scratch. 
>
>BDI systems define logical rules based on [[Modal Logic|Modal systems]] to define how an agent acts based on it's beliefs, desires and intentions.
>
>- **Beliefs** - representation of environment information
>- **Desires** - representation of objectives
>- **Intentions** - currently committed course of action

System using a "deliberation function" taking beliefs and desires as input and choosing an intention to commit to.

At each execution step, agent considers it's "termination condition" and either sticks to commitment or re-deliberates:
- Has the goal already been accomplished?
- Did something change that makes the goal unachievable?
- Is the underlying desire or priority still relevant?

#### References
- [[BDI Agents From Theory to Practice]]