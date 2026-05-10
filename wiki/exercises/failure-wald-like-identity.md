---
type: exercise
tags: [exercise, renewal-process]
sources: [lecture-notes-ch5]
related: [renewal-process, sampling-paradox]
---

# Failure of Wald-like Identity for S_N(t)

## Problem

Show that in general
$$
\mathbb{E}[S_{N(t)}]\neq \mathbb{E}[X]\mathbb{E}[N(t)].
$$

## Solution

The tempting Wald-like identity fails because $N(t)$ is not independent of the renewal intervals $X_i$. A large value of $N(t)$ implies the observed intervals before $t$ were collectively short.

One counterexample from the source is to take
$$
X_i=\begin{cases}
1 & \text{with probability }p,\\
a & \text{with probability }1-p,\quad a\geq2,
\end{cases}
$$
and set $t=1.5$. Then $S_{N(t)}$ can only include renewals that have occurred by $t$, so the stopped sum is biased toward the short interval value $1$; the product $\mathbb{E}[X]\mathbb{E}[N(t)]$ still uses the unconditional mean interval length.

The valid nearby identity is instead
$$
\mathbb{E}[S_{N(t)+1}]=\mathbb{E}[X]\mathbb{E}[N(t)+1],
$$
proved by the renewal argument.

## Concepts

- [[concepts/renewal-process|Renewal Process]]
- [[concepts/sampling-paradox|Sampling Paradox]]
- [[concepts/renewal-equation|Renewal Equation]]

## Sources

- [[sources/lecture-notes-ch5]]
