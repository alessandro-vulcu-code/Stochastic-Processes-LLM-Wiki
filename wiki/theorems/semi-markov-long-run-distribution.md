---
type: theorem
tags: [theorem, semi-markov-processes]
sources: [lecture-notes-ch5]
related: [semi-markov-process, stationary-distribution]
---

# Semi-Markov Long-Run Distribution

**A semi-Markov state's real-time probability is proportional to embedded-chain visit frequency times mean sojourn time.**

## Statement (Formal)

Let $\pi_j$ be the stationary distribution of the embedded Markov chain and $\mu_j$ the mean sojourn time in state $j$. Then
$$
P_j=\lim_{t\to\infty}\mathbb{P}[Z(t)=j]
=\frac{\pi_j\mu_j}{\sum_i\pi_i\mu_i}.
$$

The source also states the regenerative form
$$
P_i=\frac{\mu_i}{\mu_{ii}}.
$$

## Proof Sketch

Visits to state $j$ define regeneration cycles. The fraction of real time spent in $j$ is expected time in $j$ during a cycle divided by expected cycle length. The embedded-chain identity $\pi_j\mu_{jj}=\sum_i\pi_i\mu_i$ yields the computable formula.

## Conditions

The embedded chain must have a stationary distribution and mean sojourn times must be finite.

## Consequences

Unlike ordinary Markov chains, long-run real-time mass depends on both visit frequency and holding duration.

## Related Theorems

- [[renewal-reward-theorem]]

## Sources

- [[sources/lecture-notes-ch5]]

