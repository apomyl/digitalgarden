---
publish: true
created: 2026-09-23T10:01:33.105Z
modified: 2026-10-21T18:03:39.159Z
tags:
  - ai
  - school
  - machinelearning
  - intelligentagents
---

> [!definition] Reinforcement Learning
>
> > _"Learning to solve [[Markov Decision Process|sequential decision problems]] through repeated interaction with an environment"_
>
> A branch of [[Machine Learning]] where [[Autonomous Agents]] learn to make decisions through trial and error.
>
> Through interaction with an environment, the agent receives [[Reward Functions|rewards]] or is penalised, with the goal of discovering the best strategy to maximise cumulative rewards over time.
>
> A [[Policy|policy]] $\pi$ chooses actions; the agent’s goal is to learn a policy that maximises reward over time.

Expand to multiple agents - [[Multi-agent Reinforcement Learning]]

> [!question] When do we need to apply learning?
> When we know the game we can apply [[Game Theory in Agent Systems]].
>
> When the game is unknown (e.g. How good is each action?) we apply reinforcement learning for agent to deduce best strategy.

Agents can be thought of as [[Multi-Armed Bandit|multi-armed bandits]], when we add a state that changes with bandit actions – we have reinforcement learning.

> [!tldr] Expected return and Value functions
> We use an [[Reward Functions|expected discounted return]] $u_{t}$ with the goal of finding a policy $\pi$ that maximises the expectation $\mathbb{E}_{\pi}[u_{t}]$.
>
> We can use different "value functions" to quantify the expected total long-term reward of states and actions under a given policy.
>
> **State-value function:**
> $V^{\pi}(s)=\mathbb{E}_\pi[u_{t} \, | \, s_{t}=s]$
> "How good is it to be in state $s$, if I follow policy $\pi$ from here on?"
>
> **State-action value function**
> $Q^{\pi}(s,a)=\mathbb{E}_\pi[u_{t} \, | \, s_{t}=s, a_{t}=a]$
> "How good is it to take action $a$ in state $s$, then follow $\pi$?"
>
> The return decomposes recursively, $u_{t}=r_{t}+\gamma u_{t+1}$, so values do too: [[Bellman Equation]]

> [!success] Optimal value function and greedy policies
> $V^*(s) = \max_\pi V^\pi(s), \quad Q^*(s, a) = \max_\pi Q^\pi(s, a)$
>
> - A policy that acts **greedily** with respect to $Q^*$ is an **optimal policy**:
>
> $\pi^*(s) = \arg\max_{a \in A} Q^*(s, a)$
>
> if we find $Q^*$ we can always act optimally

> [!question] Prediction vs Control?
> Agents have different ways to treat both, prediction for evaluating actions and state and control to determine how to optimise.
>
> - Prediction - given a policy find out how good it is using value functions
> - Control - find the optimal policy by updating values

Techniques:

- [[Temporal-difference Learning]]

- [[SARSA]]

- [[Q-learning]]

#### References
