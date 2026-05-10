---
type: exercise
tags: [exercise, gobackn, transforms]
sources: [lecture-notes-ch6]
related: [gobackn-protocol, transition-generating-matrix]
---

# GoBackN Transform Throughput

## Problem

For GoBackN with i.i.d. feedback errors of probability $\delta$, build a two-metric transition generating matrix and recover throughput.

## Solution

Use $s_1$ for reward and $s_2$ for time. Success transitions contribute $s_1s_2$; failure transitions contribute $s_2^m$. The compact form is
$$
\psi(s_1,s_2)=\mathbf{P}_S s_1s_2+\mathbf{P}_F s_2^m.
$$
Then
$$
\mathbf{P}=\psi(1,1),
$$
and the reward/time row sums come from
$$
\left.\partial_{s_1}\psi\right|_{(1,1)}\mathbf{1},\qquad
\left.\partial_{s_2}\psi\right|_{(1,1)}\mathbf{1}.
$$
With stationary distribution $\pi$ of $\psi(1,1)$, throughput is
$$
\eta=
\frac{\pi\,\partial_{s_1}\psi(1,1)\mathbf{1}}
{\pi\,\partial_{s_2}\psi(1,1)\mathbf{1}}.
$$
The source simplifies this to
$$
\eta=
\frac{(1-\delta)p_{10}(m)}
{(1-\delta+m\delta)p_{10}(m)+m[(1-\delta)p_{01}+\delta p_{01}(m)]}.
$$

## Concepts

- [[concepts/gobackn-protocol]]
- [[concepts/transition-generating-matrix]]
- [[theorems/transition-generating-matrix-method]]

## Sources

- [[sources/lecture-notes-ch6]]

