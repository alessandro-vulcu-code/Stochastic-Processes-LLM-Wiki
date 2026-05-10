---
type: theorem
tags: [theorem, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [[lemma-monotonicity-survival-probabilities]], [[lemma-recurrence-criterion-state-0]], [[recurrence]]
---

# Lemma 3.7.2 — Maximal Bounded Solution

**The survival probability $Y_i$ is the largest bounded solution of the harmonic system $Z_i = \sum_j P_{ij} Z_j$.**

## Statement (Formal)

Let $Z_i$ be any solution of:
$$Z_i = \sum_{j \in S} P_{ij} Z_j, \qquad |Z_i| \leq 1$$

Then:
$$|Z_i| \leq Y_i = \lim_{n \to \infty} Y_i(n) \qquad \forall i \in S$$

Equivalently, $Y_i = \max\{Z_i : Z \text{ bounded solution of the harmonic system}\}$.

## Proof Sketch

By induction. At $n=0$:
$$|Z_i| = \left|\sum_{j \in S} P_{ij} Z_j\right| \leq \sum_{j \in S} P_{ij}|Z_j| \leq \sum_{j \in S} P_{ij} = Y_i(1)$$

Inductive step: $|Z_i| \leq Y_i(n) \Rightarrow |Z_i| \leq Y_i(n+1)$ by same argument. Taking $n \to \infty$ gives $|Z_i| \leq Y_i$. $\blacksquare$

## Conditions

- $S$ any subset of the state space.
- Bounded solutions: $|Z_i| \leq 1$.

## Consequences

- If a nonzero bounded solution exists, then $Y_i > 0$ for some $i$, meaning the chain has positive probability of staying in $S$ forever — implying transience.
- If the only bounded solution is $Z_i = 0$, then $Y_i = 0$ — the chain surely leaves $S$, implying recurrence.
- Together with [[lemma-recurrence-criterion-state-0]], this gives the recurrence/transience criterion via solvability of the harmonic system.

## Related Theorems

- [[lemma-monotonicity-survival-probabilities]] — establishes $Y_i$ exists.
- [[lemma-recurrence-criterion-state-0]] — uses this to characterize recurrence.
- [[recurrence-criterion]] — equivalent criterion via $\sum P_{ii}^{(n)}$.

## Sources

- [[sources/lecture-notes-ch3]] — §3.7, Lemma 3.7.2.
