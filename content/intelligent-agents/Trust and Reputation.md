---
id: 202610181557
aliases:
  - Trust
  - Reputation
tags:
  - intelligentagents
  - school
---
>[!definition] Trust
>A judgement typically made by one [[Agents|agent]] about another agent or principal in a particular context.
>This:
>- is one-sided / local
>- is contextual
>- can combine experience, guarantees and risk

>[!definition] Reputation
>An aggregated social assessment, built from multiple reports or observed interactions
>This:
>- is aggregated across many interactions
>- may combine reports from several agents
>- is often used as evidence for trust
>

Side Note - use a Beta-Style estimator for low sample sizes when calculating trust
$$\hat{t}=\frac{r+1}{r+s+2}$$
Example:
Raw rate doesn't provide a good indicator for trust.

| Provider | Good (r) | Bad (s) | Raw rate |
| -------- | -------- | ------- | -------- |
| A        | 1        | 0       | 1.00     |
| B        | 95       | 5       | 0.95     |
$\hat{t}_{A}=0.67$ and $\hat{t}_{B}=0.94$

#### References