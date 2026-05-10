---
type: theorem
tags: [theorem, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [recurrence, first-passage-time]
---

# Recurrence Criterion

**A state is recurrent exactly when the sum of its return probabilities diverges.**

## Statement (Formal)

For a Markov-chain state $i$,
$$
i\text{ is recurrent}
\quad\Longleftrightarrow\quad
\sum_{n=1}^{\infty}P_{ii}^{(n)}=\infty.
$$
Equivalently, $i$ is transient iff the same sum is finite.

## Proof Sketch

The expected number of returns to $i$ is the sum of the probabilities of being in $i$ at each future time. For a transient state this expected count is geometric with finite mean $f_{ii}/(1-f_{ii})$; for a recurrent state the chain returns infinitely often with probability one, forcing divergence.

## Conditions

The criterion is stated for discrete-time Markov chains.

## Consequences

It converts recurrence classification into a series test on $n$-step transition probabilities.

## Related Theorems

- [[basic-limit-theorem]]
- [[transience-criterion]]

## Sources

- [[sources/lecture-notes-ch3]]

