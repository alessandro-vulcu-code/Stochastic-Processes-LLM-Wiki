---
type: source
slug: lecture-notes-ch1
title: Chapter 1 - Probability and Statistics
author: Unknown
date: 2020
source-type: lecture-notes
tags: [probability, statistics, stochastic-processes]
ingested: 2026-05-10
---

# Chapter 1 - Probability and Statistics

## Summary

This chapter supplies the probability toolkit used throughout the stochastic-processes notes. It begins with the definition of a [[concepts/stochastic-process|stochastic process]] and a chain, then reviews [[concepts/sample-space|sample spaces]], [[concepts/event|events]], [[concepts/random-variable|random variables]], CDFs, PDFs, [[concepts/expected-value|expectation]], moments, variance, joint distributions, [[concepts/independence-of-rvs|independence]], and conditioning.

The chapter emphasizes transforms as reusable computational tools. The [[concepts/characteristic-function|characteristic function]] represents a distribution by its Fourier transform, turns [[concepts/convolution|convolution]] into products, and recovers moments by differentiation. The [[concepts/probability-generating-function|probability generating function]] plays the same role for nonnegative integer-valued variables and is central for random sums.

It also collects the main distributions used later: [[concepts/bernoulli-distribution|Bernoulli]], [[concepts/binomial-distribution|Binomial]], [[concepts/geometric-distribution|Geometric]], [[concepts/poisson-distribution|Poisson]], [[concepts/normal-distribution|Normal]], [[concepts/exponential-distribution|Exponential]], [[concepts/uniform-distribution|Uniform]], and [[concepts/gamma-distribution|Gamma]]. The exponential and geometric distributions are highlighted through memorylessness, while the Poisson distribution is introduced as the limit law for rare events.

## Key Concepts Introduced

- [[concepts/stochastic-process|Stochastic Process]] - process as a family of random variables indexed by a set $T$.
- [[concepts/stationary-process|Stationary Process]] - process law/distributions invariant under time shifts in the sense used by the notes.
- [[concepts/sample-space|Sample Space]] - set of possible outcomes.
- [[concepts/event|Event]] - observable subset of the sample space.
- [[concepts/random-variable|Random Variable]] - CDF/PDF, expectation, variance, and moments.
- [[concepts/expected-value|Expected Value]] - probability-weighted average and moment foundation.
- [[concepts/independence-of-rvs|Independence of Random Variables]] - factorization of joint laws.
- [[concepts/conditional-probability|Conditional Probability]] - law of total probability, conditional CDF/PDF, and iterated expectation.
- [[concepts/convolution|Convolution]] - distribution of a sum of independent variables.
- [[concepts/n-fold-convolution|n-Fold Convolution]] - repeated convolution for i.i.d. sums.
- [[concepts/characteristic-function|Characteristic Function]] - Fourier transform representation of distributions.
- [[concepts/probability-generating-function|Probability Generating Function]] - transform for nonnegative integer random variables and random sums.
- [[concepts/bernoulli-distribution|Bernoulli Distribution]] - one success/failure trial and indicator variables.
- [[concepts/binomial-distribution|Binomial Distribution]] - count of successes in independent Bernoulli trials.
- [[concepts/geometric-distribution|Geometric Distribution]] - failures before first success and discrete memorylessness.
- [[concepts/poisson-distribution|Poisson Distribution]] - rare-event count distribution with mean and variance $\lambda$.
- [[concepts/normal-distribution|Normal Distribution]] - Gaussian distribution used for limit approximations.
- [[concepts/exponential-distribution|Exponential Distribution]] - continuous memoryless lifetime law.
- [[concepts/uniform-distribution|Uniform Distribution]] - equal density on an interval.
- [[concepts/gamma-distribution|Gamma Distribution]] - sum of i.i.d. exponential variables.

## Key Theorems

- [[theorems/law-of-total-probability|Law of Total Probability]] - decomposes events over a partition.
- [[theorems/law-of-total-variance|Law of Total Variance]] - decomposes variance into within-condition and between-condition parts.
- [[theorems/memoryless-property|Memoryless Property]] - exponential survival is age-independent.
- [[theorems/poisson-limit-theorem|Poisson Limit Theorem]] - Binomial$(n,\lambda/n)$ converges to Poisson$(\lambda)$.
- [[theorems/levy-inversion-formula|Levy Inversion Formula]] - characteristic functions uniquely determine distributions.
- [[theorems/factorial-moment-formula-pgf|Factorial Moment Formula for PGFs]] - PGF derivatives give factorial moments.

## Notation

- $F_X(x)$ for CDF.
- $f_X(x)$ for PDF when the CDF is differentiable.
- $\phi_X(t)=\mathbb{E}[e^{itX}]$ for characteristic functions.
- $g(s)=\mathbb{E}[s^X]$ for PGFs.

## Critique / Gaps

The chapter is a review, so measure-theoretic foundations are intentionally omitted. Some formulas are stated informally, which is adequate for later applications but not enough for a rigorous probability theory reference.

## Wiki Pages Updated

- [[concepts/stochastic-process]], [[concepts/stationary-process]], [[concepts/sample-space]], [[concepts/event]], [[concepts/random-variable]], [[concepts/expected-value]], [[concepts/independence-of-rvs]], [[concepts/conditional-probability]], [[concepts/convolution]], [[concepts/n-fold-convolution]], [[concepts/characteristic-function]], [[concepts/probability-generating-function]], [[concepts/bernoulli-distribution]], [[concepts/binomial-distribution]], [[concepts/geometric-distribution]], [[concepts/poisson-distribution]], [[concepts/normal-distribution]], [[concepts/exponential-distribution]], [[concepts/uniform-distribution]], [[concepts/gamma-distribution]]
- [[theorems/law-of-total-probability]], [[theorems/law-of-total-variance]], [[theorems/memoryless-property]], [[theorems/poisson-limit-theorem]], [[theorems/levy-inversion-formula]], [[theorems/factorial-moment-formula-pgf]]
- [[topics/probability-statistics-review]]
- [[exercises/random-sum-pgf]], [[exercises/binomial-poisson-thinning]], [[exercises/geometric-sum-exponentials]]
