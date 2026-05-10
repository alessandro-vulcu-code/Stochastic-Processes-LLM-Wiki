---
type: theorem
tags: [theorem, probability, transforms]
sources: [lecture-notes-ch1]
related: [[concepts/characteristic-function]], [[concepts/random-variable]]
---

# Levy Inversion Formula

**Statement** The characteristic function determines the probability distribution uniquely.

## Statement (Formal)

If $\phi_X(t)=\mathbb{E}[e^{itX}]$ is the characteristic function of a random variable $X$, then the distribution function $F_X$ can be recovered from $\phi_X$ at continuity points of $F_X$ by an inversion formula.

One common form, for continuity points $a<b$, is:
$$
\mathbb{P}(a<X\leq b)
=\lim_{T\to\infty}\frac{1}{2\pi}\int_{-T}^{T}
\frac{e^{-ita}-e^{-itb}}{it}\phi_X(t)\,dt.
$$

## Proof Sketch

The source only cites the result. The standard proof treats $\phi_X$ as a Fourier transform of the probability measure and recovers interval masses by Fourier inversion with a smoothing/limit argument.

## Conditions

- Recovery is stated at continuity points of the CDF or for intervals whose endpoints are continuity points.
- Characteristic functions always exist, unlike moment generating functions.

## Consequences

- Characteristic functions uniquely identify distributions.
- Convergence of characteristic functions can be used to prove convergence in distribution.
- Sums of independent random variables can be studied through products of characteristic functions.

## Related Theorems

- [[concepts/convolution|Convolution]] via product of transforms.
- [[theorems/poisson-sum|Sum of Independent Poisson Variables]].

## Sources

- [[sources/lecture-notes-ch1]] - cites Levy inversion as the reason characteristic functions correspond one-to-one with CDFs.
