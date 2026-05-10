---
type: concept
tags: [stochastic-processes, probability, markov-chains, renewal-phenomena]
sources: [lecture-notes-ch3]
related: [[recurrence]], [[null-recurrent]], [[renewal-process]]
---

# Improper Random Variable

**An improper random variable is one that takes the value $+\infty$ with positive probability.**

## Definition

A random variable $X$ is **proper** if:
$$\lim_{x \to \infty} \mathbb{P}[X > x] = 0 \quad \Leftrightarrow \quad \mathbb{P}[X = \infty] = 0$$

$X$ is **improper** if:
$$P_\infty = \lim_{x \to \infty} \mathbb{P}[X > x] > 0 \quad \Leftrightarrow \quad \mathbb{P}[X = \infty] = P_\infty > 0$$

## Key Properties

- Expectation of a nonneg. improper r.v. always diverges:
$$\mathbb{E}[X] = \int_0^\infty \mathbb{P}[X > x]\,dx = \infty \quad \text{(continuous)}$$
$$\mathbb{E}[X] = \sum_{k=0}^\infty \mathbb{P}[X > k] = \infty \quad \text{(discrete)}$$
- The number of returns $M$ to a **recurrent** state is improper: $\mathbb{P}[M = \infty] = 1$.
- The mean return time $m_i$ for a **null recurrent** state is an improper r.v. with infinite expectation.

## Intuition

Proper r.v.s concentrate on finite values. Improper r.v.s formally allow $\infty$ as an outcome — necessary when studying recurrent Markov chains, where the number of returns is infinite with certainty, and where return times may be infinite in mean.

## Connection to Other Concepts

- [[recurrence]] — number of returns to a recurrent state is improper.
- [[null-recurrent]] — mean return time is infinite; return time itself is improper in expectation.
- [[renewal-process]] — stopped processes arise when inter-arrival times may be infinite ($F(\infty) < 1$).

## Sources

- [[sources/lecture-notes-ch3]] — §3.3, improper random variables introduced to handle return counts for recurrent states.
