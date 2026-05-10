---
type: concept
tags: [stochastic-processes, renewal-process, regenerative-processes]
sources: [lecture-notes-ch5]
related: [[concepts/renewal-process]], [[concepts/renewal-reward-process]], [[concepts/regenerative-process]]
---

# Alternating Renewal Process

**An alternating renewal process switches between states such as ON/OFF across renewal cycles.**

## Definition

Each renewal cycle has a total duration $X_i$ and a subduration $Y_i$ spent in a marked state, such as ON. Under i.i.d. cycles, the long-run fraction of time in the marked state is
$$
\frac{\mathbb{E}[Y]}{\mathbb{E}[X]}.
$$

## Key Properties

- It is a special case of a renewal-reward process with reward equal to time spent in a state.
- It computes availability, busy/idle fractions, and reliability fractions.
- The renewal cycles must be statistically equivalent.

## Intuition

Look at one typical cycle. The long-run time average is the average marked time per cycle divided by average cycle length.

## Connection to Other Concepts

Alternating renewal processes instantiate [[theorems/renewal-reward-theorem|Renewal Reward Theorem]] and motivate [[concepts/regenerative-process|Regenerative Process]] state-occupation formulas.

## Theorems

- [[theorems/renewal-reward-theorem|Renewal Reward Theorem]]

## Examples

- A component alternating between failed and operating states.
- A loss system alternating between idle and busy periods.

## Open Questions / Gaps

> [!todo] Gap - Add a comparison page for alternating renewal vs semi-Markov occupation.

## Sources

- [[sources/lecture-notes-ch5]] - ON/OFF and queueing examples.
