---
publish: true
created: 2026-10-17T19:24:46.797Z
modified: 2026-10-26T20:13:43.778Z
tags:
  - intelligentagents
  - school
---

> [!garden] Summary
> This page breaks down key concepts of a [[Normative Multi-Agent Systems|Normative]] approach to [[Multi-Agent Systems]].

> [!definition] Formal Definition
> Each norm involves a:
>
> - subject - who is responsible
> - object - who is owed
> - context - where the norm applies
> - antecedent - the triggering condition
> - consequent - the goal
>
> ![[media/Normative Concepts-1792265314123.webp|418x237]]
>
> Example: In an online bookstore (**Context**), the seller (**Subject**) is obligated to the buyer (**Object**) to dispatch the order (**Consequent**) once payment is received (**Antecedent**)

##### Norm Types

> [!definition] [[Commitment-Based Communication|Commitment]]
> The subject is committed to the object that if the antecedent holds they will bring about the consequent
>
> $C(sbj, obj, ant, con)$
> _if $ant$ happens $s$ is committed to $o$ to bring about $con$_

> [!definition] Authorisation
> The object authorises the subject to bring about the consequent if the antecedent holds
> $A(sbj, obj, ant, con)$
> _if $ant$ happens, $obj$ authorises $sbj$ to bring about $con$_

> [!definition] Prohibition
> The object prohibits the subject from bringing about the consequent if the antecedent holds
>
> $P(sbj, obj, ant, con)$
> _if $ant$ happens, $obj$ prohibits $sbj$ from bringing about $con$_

> [!definition] Sanction
> The object would sanction the subject by bringing about the consequent if the antecedent holds
> $S(sbj, obj, ant, con)$
> _if $ant$ happens, $obj$ punishes $sbj$ by bringing about $con$_

> [!definition] Power
> The object empowers the subject to bring about the  consequent by bringing about the antecedent. A power is the ability to alter the norms between two or more principals
> $Pow(sbj, obj, ant, con)$
> _if $ant$ is satisfied, $obj$ empowers $sbj$ to alter/create/terminate a norm $con$_

- for commitment the subject is accountable
- for prohibition the subject is accountable
- for authorisation the object is accountable

##### Norm Lifecycle

![[media/Sociotechnical Systems and Social Norms-1790674406151.webp]]

Rule exists for a certain antecedent, if that doesn't come about it expires or it could be satisfied before it comes about. When antecedent comes about, norm is in force, which then can be satisfied or violated, it can also be suspended and resumed at any point.

Lifecycle for prohibition:
![[media/Normative Concepts-1793045503106.webp|551]]

Lifecycle for authorisation:
![[media/Normative Concepts-1793045514145.webp|551]]

#### References
