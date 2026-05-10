---
type: concept
tags: [stochastic-processes, regenerative-processes]
sources: [lecture-notes-ch5]
related: [renewal-process, renewal-reward-process, semi-markov-process]
---

# Regenerative Process

**A regenerative process is a stochastic process that probabilistically restarts at random regeneration times.**

## Definition

A process $\{X(t)\}$ is regenerative if there are times $S_1,S_2,\ldots$ such that, after each $S_k$, the future evolution is statistically a fresh copy of the process after time $0$.

## Key Properties

- Regeneration times form an embedded renewal process.
- State-time probabilities can be computed by expected time in a state per expected cycle length.
- Markov chains regenerate when they return to a reference state.

## Intuition

The process may have complicated motion inside a cycle, but cycles repeat statistically.

## Connection to Other Concepts

- [[renewal-process]] tracks regeneration times.
- [[renewal-reward-process]] computes time averages inside cycles.
- [[semi-markov-process]] is a regenerative process at visits to a state.

## Theorems

- [[renewal-reward-theorem]]
- [[semi-markov-long-run-distribution]]

## Examples

- Alternating renewal systems.
- Queue busy/idle cycles.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch5]] - regenerative process explanation.

