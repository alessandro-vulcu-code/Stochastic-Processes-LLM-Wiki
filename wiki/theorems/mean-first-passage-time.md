---
type: theorem
tags: [theorem, markov-chains]
sources: [lecture-notes-ch2]
related: [first-passage-time, first-step-analysis]
---

# Mean First Passage Time

**Mean first-passage times satisfy a linear first-step system.**

## Statement (Formal)

For target state $j$,
$$
\mathbb{E}[\theta_{ij}]
=1+\sum_{k\neq j}P_{ik}\mathbb{E}[\theta_{kj}].
$$

## Proof Sketch

On the first step, either the chain reaches $j$ immediately, or it moves to some $k\neq j$ and still must reach $j$ from there. Average the decomposition.

## Conditions

The expectation must be finite for the equation to give a finite solution.

## Consequences

Mean hitting times can be computed by solving linear equations.

## Related Theorems

- [[basic-limit-theorem]]

## Sources

- [[sources/lecture-notes-ch2]]

