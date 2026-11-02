---
publish: true
created: 2026-11-01T16:22:46.769Z
modified: 2026-11-01T17:11:27.146Z
tags:
  - project
---

> [!garden]
>
> I completed my internship at [Safer Industries](https://linktr.ee/saferindustries) throughout the summer of 2026, working on a full-stack prototype for a notes application, with a focus on innovation, automation and speed.

> [!tldr] Technical Implementation
>
> The basic idea of the application was to treat each note as atomic and automatically link it with others, organise the notes in a helpful way to support learning / the building ideas. Aimed not to use LLMs and have everything running locally for privacy.
>
> **Frontend**
>
> - Next.js framework - react/typescript
> - Graph visualisations using react-force-graph
>
> **Backend**
>
> - Python (FastAPI server)
> - FastText classification model to classify notes based on language/tone
> - NLP techniques to extract entities (spacy), tags (embeddings w/ IPTC topic list), topic clusters ([[BERTopic]])

#### References
