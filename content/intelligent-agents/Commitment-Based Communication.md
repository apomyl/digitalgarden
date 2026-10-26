---
publish: true
created: 2026-10-18T14:07:47.337Z
modified: 2026-10-26T20:14:04.416Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> A communication strategy in [[Multi-Agent Systems]] based around commitments ([[Norms in Agent Systems|Norms]])

Formally:
$C(sbj, obj, ant, con)$

- subject - who is responsible
- object - who is owed
- antecedent - the triggering condition
- consequent - the final state / goal

**Subject** is committed to the **object** that if the **antecedent** holds, the subject will bring about the **consequent**.

> [!success] Benefits
>
> - Public social state
> - Flexible ways to be satisfied
> - Accountability without hidden beliefs

> [!tldr] Commitment Operations
>
> - CREATE - subject makes a commitment hold
> - CANCEL - subject withdraws its own commitment, if permitted
> - RELEASE - object frees the subject from the commitment
> - DELEGATE - subject transfers responsibility to another subject
> - ASSIGN - object transfers "creditor" role to another object
>
> Not a commitment operation:
>
> - DECLARE - announces a fact

![[media/Intelligent Agents Lecture 2026-09-29-1790687964211.webp]]

#### References/Relevant

- [[Normative Concepts]]
- [[A Social Semantics for Agent Communication Languages]]
