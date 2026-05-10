---
type: exercise
tags: [exercise, renewal-process, reliability]
sources: [lecture-notes-ch5]
related: [renewal-reward-process, exponential-distribution]
---

# Two-Component Parallel System

## Problem

Two independent components alternate between down and operating. Component $i$ repairs at rate $\alpha_i$ and fails at rate $\beta_i$. The system works if at least one component operates. Find long-run failed fraction, mean failed duration, mean cycle duration, and mean operating duration between failures.

## Solution

For component $i$, the long-run down probability is
$$
\frac{\beta_i}{\alpha_i+\beta_i}.
$$
Independence gives system failed fraction
$$
\left(\frac{\beta_A}{\alpha_A+\beta_A}\right)
\left(\frac{\beta_B}{\alpha_B+\beta_B}\right).
$$

Once both are down, recovery happens at the minimum of two independent exponentials with rates $\alpha_A,\alpha_B$, so
$$
\mathbb{E}[\mathrm{down\ duration}]=\frac{1}{\alpha_A+\alpha_B}.
$$
Using failed fraction = mean down duration / mean cycle duration,
$$
\mathbb{E}[\mathrm{cycle}]
=\frac{1/(\alpha_A+\alpha_B)}
{\left(\frac{\beta_A}{\alpha_A+\beta_A}\right)
\left(\frac{\beta_B}{\alpha_B+\beta_B}\right)}.
$$
Finally,
$$
\mathbb{E}[\mathrm{operating\ duration}]
=\mathbb{E}[\mathrm{cycle}]-\frac{1}{\alpha_A+\alpha_B}.
$$

## Concepts

- [[concepts/renewal-reward-process]]
- [[concepts/exponential-distribution]]

## Sources

- [[sources/lecture-notes-ch5]]

