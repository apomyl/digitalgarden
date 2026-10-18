---
id: 202610181307
Author:
  - Munindar P. Singh
aliases:
tags:
  - intelligentagents
  - school
---
>[!garden] Summary
>This paper sets out to formalise the semantics of a social approach to [[Agent Communication Languages]] proposed in [[Agent Communication Languages Rethinking the Principles]] through a [[Commitment-Based Communication|commitment-based]] approach to communication.
#### Notes

- Continuing to build on his previous ideas about ACLs, Singh presents social semantics focusing on interactions between agents based on social commitments and temporal logic
- He reiterates that agents in [[Multi-Agent Systems|MAS]] must be:
	- autonomous - few constraints on behaviour
	- heterogeneous - few constraints on construction
- And that previous attempts at formal semantics and ACLs fail to maintain these properties

What makes good ACL Semantics?
- Formal
	- clarity of specifications to guide implementers
	- assurance of software
- Declarative
	- describing what rather than how
	- makes it more easily applied to a variety of settings
- Verifiable
	- possible to determine if an agent is acting according to a given semantic
- Meaningful
	- "based on some intuitive appreciation of communications and not treating communications merely as arbitrary tokens to be ordered in some way"
	- I imagine he means [[Communicative Acts]]

While studying ACLs I've been wondering about their important today, in a world of LLMs that communicate in natural language, are they obsolete? Singh makes a comment which I find interesting and would need to explore further to see if it still holds today:
- "For example, English descriptions of communications (quite common in practice) are not formal, finite-state machines (FSMs) are not declarative or meaningful, mentalistic approaches are not verifiable, and temporal logics (if applied to tokens directly) and formal grammar representations of sequences of tokens are not meaningful."
- Although he was not directly talking about agents communicating in natural language, the issues he raises seem to hold. The lack of formality in allowing agents to communicate in natural language means that there is no assurance, agent communication could result in any number of things happening, agents could hallucinate commitments or ignore certain aspects of their interactions because they personally didn't believe that what was said was a communicative act e.g. they ignore an implicit request from another agent

More arguments about mentalisitic approach not being sufficient and social approach being superior.

The mentalistic approach (inspired by [[Speech Acts]]) is based on the speaker's intent and private mental state. *"Under this doctrine, the illocution is what the speaker believed or intended it to be."*
Singh proposes another philosophical approach based on ideas by Habermas, which associates three meanings to communicative acts:
- objective - that the communication is true
- subjective - that the communication is sincere
- practical - that the speaker is justified in making the communication
He argues that this is a better model for communication as communication is inherently public and every communication is tested through these 3 *validity claims*.

>[!quote] 
>"In conversation, each of the above claims may be challenged and shown to be false. However, even if false, these claims are staked with each communication, which is why they can be meaningfully questioned. The claims involve different aspects of meaning including the subjective, but by fact of being claims in a conversation, they are public and social. If I tell you something, I am committed to being accurate, and you are entitled to check if I am. I am also committed to being sincere, even though you may not be able to detect my insincerity unless you can infer what I believe, e.g., through contradictory statements that I make at about the same time. In general, in open environments, agents cannot safely determine whether or not another agent is sincere."

He then sets out a formal language based on Computation Tree Logic. What's important to note is:
- every commitment has 3 parties: debtor, creditor and context
#### References