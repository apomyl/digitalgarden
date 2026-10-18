---
id: 202610171124
Author:
  - Anand S. Rao
  - Michael P. Georgeff
aliases:
tags:
  - scientific-papers
  - intelligentagents
---
>[!garden] Summary
>The paper sets out to define and explain an [[Agent Architecture]]: [[Belief-Desire-Intention]] and how it can be applied logically and practically.
>
>BDI is a better alternative to [[Sense-Decide-Act]] as it performs better in a dynamic environment.
#### Notes

Characteristics of a real-world environment:
- environment is non-deterministic
- agent is non-deterministic
- possibly many different objectives
- (best) actions are dependant on environment by independent of internal state
- environment can only be sensed locally
- speed of agent reasoning is within reasonable bounds of the rate of changes happening in environment

Belief - component of system representing representing available information from environment
Desire - component representing information about objectives and payoffs
Intention - component representing output of most recent call to selection function

Selection function - choose best action
Deliberation function - choose best sequence of actions

##### Dilemma that Intentions solve

Considering two approaches: Decision-Theoretic and Computer Science
- decision-theory - re-run selection function every time a change happens
- computer science - finish execution ignoring changes
Without intentions the system fails because the environment may change significantly during execution of either the selection function or the action itself.

We use intentions to create a hybrid where we store the initial chosen action and then decide whether to **commit** or not.

##### Tree representation

Model system as a branching decision tree with following nodes:
- Decision - agent choices
- Chance - uncertainty resolved by environment (changes)
- Terminal - outcome states (assigned payoffs)
Through this model we can identify objectives through different paths and apply payoffs to each path

We transform this structure by eliminating chance nodes, splitting into multiple different trees where each is a **possible world** and is assigned a probability and has a corresponding payoff.

We split this further into two [[Accessibility Relations]]:
- Belief-Accessible worlds based on probabilities
- Desire-Accessible worlds based on payoffs
Create third:
- Intention-Accessible worlds by applying the deliberation function on each desire-accessible world

We can examine the static relationships between worlds in 2 different dimensions:
- sets of possible worlds
- structure of possible worlds
Thus we can have 4 different relationships:
- one being a subset of the other and vice versa
- their intersections being null or non-null
Now combining the 3 sets and 4 relations we have 12 different BDI systems, including:
- Realism - if an agent believes a proposition, it will desire it
- Strong Realism - if an agent desires achieve a proposition, it will believe the proposition to be an option
- Weak Realism - if an agent desires to achieve a proposition, it will not believe the negation of the proposition to be inevitable
#### References
