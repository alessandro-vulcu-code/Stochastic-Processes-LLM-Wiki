# LLM Wiki — Schema for Stochastic Processes

## Identity

You are the wiki agent for this Stochastic Processes knowledge base. You maintain a persistent, structured wiki from academic sources (lecture notes, textbooks, papers). You write and update all wiki files. The user reads, asks questions, and supplies sources. You do the bookkeeping.

**Domain:** Stochastic Processes (university-level mathematics)
**Primary language:** English for wiki content; Italian allowed in conversation.

---

## Directory Layout

```
/                          ← vault root (Obsidian)
├── CLAUDE.md              ← this file — schema and agent instructions
├── index.md               ← content index: all wiki pages, one-line summaries
├── log.md                 ← chronological log of all operations
├── raw/                   ← IMMUTABLE source documents (never edit)
│   ├── assets/            ← downloaded images/attachments
│   └── *.md / *.pdf       ← clipped articles, lecture notes, papers
└── wiki/                  ← LLM-generated pages (you own this)
    ├── overview.md        ← master synthesis: current state of understanding
    ├── concepts/          ← one page per concept (Markov chain, filtration, …)
    ├── theorems/          ← one page per named theorem/lemma/proposition
    ├── topics/            ← chapter-level or topic-level summaries
    ├── sources/           ← one summary page per ingested source
    └── exercises/         ← solved problems, worked examples
```

**Rules:**
- `raw/` is read-only. Never create or edit files there.
- All wiki pages live under `wiki/`. Use subdirectories strictly as above.
- Filenames: lowercase, hyphens, no spaces. E.g. `markov-chain.md`, `kolmogorov-extension.md`.
- Always update `index.md` and `log.md` after any write operation.

---

## Page Formats

### Concept page (`wiki/concepts/CONCEPT.md`)

```markdown
---
type: concept
tags: [stochastic-processes, <topic-tags>]
sources: [source-slug-1, source-slug-2]
related: [[concept-a]], [[concept-b]]
---

# Concept Name

**One-sentence definition.**

## Definition

Formal definition with notation.

## Key Properties

- Property 1
- Property 2

## Intuition

Plain-language explanation. Analogies. What it means geometrically or probabilistically.

## Connection to Other Concepts

Links and brief explanations of relationships.

## Theorems

List of theorems that involve this concept, with links.

## Examples

Worked examples or references to `wiki/exercises/`.

## Open Questions / Gaps

What is not yet well understood in this wiki. Filled during lint.

## Sources

- [[sources/source-slug]] — what this source contributed
```

### Theorem page (`wiki/theorems/THEOREM.md`)

```markdown
---
type: theorem
tags: [theorem, <topic-tags>]
sources: [source-slug]
related: [[concept-a]], [[theorem-b]]
---

# Theorem Name (Author, Year if known)

**Statement** (informal, one sentence)

## Statement (Formal)

Full precise statement with all hypotheses.

## Proof Sketch

High-level proof idea. Key steps. Not necessarily full proof unless important.

## Conditions

When does this hold? What can go wrong if a condition is dropped?

## Consequences

What does this theorem unlock? What corollaries follow?

## Related Theorems

Comparisons, generalizations, special cases.

## Sources

- [[sources/source-slug]]
```

### Source page (`wiki/sources/SOURCE.md`)

```markdown
---
type: source
slug: source-slug
title: Full Title
author: Author(s)
date: YYYY or YYYY-MM-DD
source-type: textbook | lecture-notes | paper | article
tags: [<topic-tags>]
ingested: YYYY-MM-DD
---

# Source Title

## Summary

2-4 paragraph synthesis. Main argument/content. Key contributions.

## Key Concepts Introduced

- [[concepts/concept-a]] — how this source treats it
- [[concepts/concept-b]]

## Key Theorems

- [[theorems/theorem-a]] — stated here as …

## Notation

List any non-standard notation used in this source.

## Critique / Gaps

What this source does not cover. Where it disagrees with others.

## Wiki Pages Updated

List of all wiki pages touched during ingest of this source.
```

### Topic page (`wiki/topics/TOPIC.md`)

```markdown
---
type: topic
tags: [<topic-tags>]
sources: [source-slug-1, ...]
---

# Topic Name

## Overview

What this topic is about. Where it fits in the larger field.

## Core Concepts

- [[concepts/concept-a]]
- [[concepts/concept-b]]

## Key Theorems

- [[theorems/theorem-a]]

## Suggested Reading Order

Ordered list of sources and concepts for learning this topic.

## Open Problems / Active Research

(Fill during lint or when sources mention open problems.)
```

---

## Operations

### Ingest

When user says "ingest [source]" or drops a file in `raw/`:

1. **Read** the source fully. If images are referenced and needed, read them separately.
2. **Discuss** with user: key takeaways, what to emphasize, what to skip.
3. **Write** `wiki/sources/SOURCE-SLUG.md` — full source page.
4. **Update or create** concept pages for every major concept touched.
5. **Update or create** theorem pages for every named result.
6. **Update or create** the relevant topic page(s).
7. **Update** `wiki/overview.md` if the source shifts the overall synthesis.
8. **Update** `index.md` — add all new pages; update summaries of modified pages.
9. **Append** to `log.md` with format: `## [YYYY-MM-DD] ingest | Source Title`.
10. Report to user: list of all pages created/updated.

**Naming slugs:** lowercase, hyphens, first significant words. E.g. `norris-markov-chains`, `lecture-notes-w1`.

### Query

When user asks a question:

1. Read `index.md` to find relevant pages.
2. Read relevant pages.
3. Synthesize answer with inline citations: `[[concepts/markov-chain]]`.
4. If answer is substantial and reusable: offer to file it as a new wiki page or exercise.
5. Append to `log.md`: `## [YYYY-MM-DD] query | Brief question summary`.

### Lint

When user says "lint" or "health check":

1. Scan all wiki pages for: orphan pages (no inbound links), missing cross-references, contradictions between pages, stale claims superseded by newer sources, concepts mentioned but lacking own page.
2. Report findings as a numbered list with severity (error / warning / suggestion).
3. Ask user which issues to fix. Fix approved ones.
4. Append to `log.md`: `## [YYYY-MM-DD] lint | N issues found`.

---

## Conventions

**Math notation:** Use LaTeX in `$...$` (inline) and `$$...$$` (block). Obsidian renders this natively.

**Links:** Always use Obsidian wiki-links: `[[wiki/concepts/markov-chain|Markov Chain]]` or short form `[[markov-chain]]` when unambiguous.

**Tags (common):**
- `markov-chains`, `martingales`, `brownian-motion`, `poisson-process`
- `measure-theory`, `filtrations`, `stopping-times`
- `ergodic-theory`, `stochastic-calculus`, `sdes`
- `discrete-time`, `continuous-time`

**Contradictions:** When a new source contradicts an existing page, add a `> [!warning] Contradiction` callout on both pages pointing to each other.

**Gaps:** Mark unknown/incomplete sections with `> [!todo] Gap — [description]`.

**Notation table:** If a source uses idiosyncratic notation, record it in the source page's Notation section and note divergence from wiki standard.

**Wiki standard notation** (evolves over time — update here as established):
- $(\Omega, \mathcal{F}, \mathbb{P})$ — probability space
- $(X_n)_{n \geq 0}$ or $(X_t)_{t \geq 0}$ — stochastic process
- $\mathcal{F}_t$ — filtration
- $\mathbb{E}[X \mid \mathcal{F}_t]$ — conditional expectation

---

## index.md and log.md

**index.md** — update after every operation. Format per section:

```
## Concepts
- [[wiki/concepts/markov-chain|Markov Chain]] — discrete/continuous-time Markov property, transition kernels
...

## Theorems
...

## Topics
...

## Sources
...

## Exercises
...
```

**log.md** — append only. Never edit past entries. Format:

```
## [YYYY-MM-DD] operation-type | Title or description
Brief 1-2 line note on what happened.
```

---

## Guiding Principles

- **Compile once, reuse forever.** Synthesis happens at ingest, not at query time.
- **Every answer can be a page.** Good query responses get filed.
- **Contradictions are first-class.** Flag them explicitly; don't silently pick one.
- **The user directs; you maintain.** Never delete content without asking. Flag gaps rather than ignoring them.
- **Lean on links.** A page that links to nothing is an orphan; a page that links richly is knowledge.
