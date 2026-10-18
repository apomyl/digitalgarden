---
id: 202610171238
aliases:
tags:
  - intelligentagents
  - school
---
>[!definition] 
>An extension of classic logical (Boolean), adding new operators to represent the "mode" (context or condition) under which a proposition is true.

Basic Kripke Semantics (K):
- Standard classical logic (AND, OR, NOT)
- Necessity operator ($\Box$): $\square P$ means "P is necessarily true"
	- always true no matter what
- Possibility operator ($\Diamond$): $\Diamond P \equiv \neg \Box \neg P$
	- P is true in atleast one world
	- "It is possible that $P$" just means "It is NOT necessarily true that $P$ is false."
- Axiom K (Distribution): $\Box(p \to q) \to (\Box p \to \Box q)$
	- if an implication is necessary, and the premise is necessary, the conclusion must also be necessary
- Axiom N (Necessitation): $\text{If } P \text{ is a valid theorem/tautology, then } \Box P \text{ is also a theorem.}$
	- if P is logically true always then it must be valid across all worlds

Add-on axioms to form different Modal Systems:
- Consistency (D): $\Box p \to \Diamond p$ (or $\text{Bel}(p) \to \neg \text{Bel}(\neg p)$)
	- you cannot hold contradictory views
- Truth (T): $\Box p \to p$
	- if something is known, it must be true in reality
- Positive Introspection (4): $\Box p \to \Box \Box p$
	- if you know $p$, you are aware that you know $p$
- Negative Introspection (5): $\neg \Box p \to \Box \neg \Box p$
	- if you do not know/believe $p$, you are aware that you don't

In [[Belief-Desire-Intention]] agents we use the KD45 Modal System.
#### References
- [[BDI Agents From Theory to Practice]]
- A Completeness Theorem in Modal Logic, Saul A. Kripke