---
type: source
slug: lecture-notes-ch2
title: Chapter 2 - Markov Chains
author: Unknown
date: 2020
source-type: lecture-notes
tags: [markov-chains, discrete-time]
ingested: 2026-05-10
---

# Chapter 2 - Markov Chains

## Summary

This chapter introduces discrete-time, countable-state [[concepts/markov-chain|Markov chains]]. It defines the [[concepts/markov-property|Markov property]], [[concepts/homogeneous-markov-chain|homogeneous transition probabilities]], the [[concepts/transition-matrix|transition matrix]], and the factorization of finite path probabilities from the [[concepts/initial-distribution|initial distribution]] and one-step transition probabilities.

The chapter then develops the core computational methods: [[theorems/chapman-kolmogorov|Chapman-Kolmogorov equations]], [[concepts/n-step-transition-probability|n-step transition probabilities]], first-step analysis for absorption probabilities and mean absorption times, two-state chain powers, random walks, gambler's ruin, success-run models, and first passage times.

It also introduces queueing chains, especially [[concepts/m-g-1-queue|M/G/1]] and [[concepts/g-m-1-queue|G/M/1]] models, as embedded Markov chains sampled at event epochs.

The final part gives the matrix formulation for absorbing chains. With transient block $\mathbf{Q}$ and absorbing block $\mathbf{R}$, the [[concepts/fundamental-matrix|fundamental matrix]] $\mathbf{W}=(I-\mathbf{Q})^{-1}$ gives expected transient-state visits, mean time to absorption, and absorption probabilities.

## Key Concepts Introduced

- [[concepts/markov-chain|Markov Chain]] - future independent of past given present.
- [[concepts/markov-property|Markov Property]] - conditional independence of future and past given present.
- [[concepts/homogeneous-markov-chain|Homogeneous Markov Chain]] - time-independent transition law.
- [[concepts/initial-distribution|Initial Distribution]] - starting-state probability vector.
- [[concepts/transition-matrix|Transition Matrix]] - row-stochastic matrix of one-step probabilities.
- [[concepts/n-step-transition-probability|n-Step Transition Probability]] - entries of $\mathbf{P}^n$.
- [[concepts/first-step-analysis|First-Step Analysis]] - recursive conditioning on $X_1$.
- [[concepts/first-passage-time|First Passage Time]] - first hitting time of a target state.
- [[concepts/absorbing-markov-chain|Absorbing Markov Chain]] - transient states plus absorbing states.
- [[concepts/fundamental-matrix|Fundamental Matrix]] - expected visits before absorption.
- [[concepts/random-walk|Random Walk]] - nearest-neighbour Markov-chain model.
- [[concepts/m-g-1-queue|M/G/1 Queue]] - Poisson arrivals, general service, one server.
- [[concepts/g-m-1-queue|G/M/1 Queue]] - general arrivals, exponential service, one server.

## Key Theorems

- [[theorems/markov-chain-factorization|Markov Chain Factorization]] - $\mathbf{P}$ and initial law determine all path probabilities.
- [[theorems/chapman-kolmogorov|Chapman-Kolmogorov Equations]] - $n$-step probabilities are matrix powers.
- [[theorems/two-state-chain-n-step|Two-State Chain n-Step Formula]] - explicit decomposition into stationary and transient components.
- [[theorems/mean-first-passage-time|Mean First Passage Time]] - linear first-step system for expectations.
- [[theorems/fundamental-matrix|Fundamental Matrix Theorem]] - $\mathbf{W}=(I-\mathbf{Q})^{-1}$.
- [[theorems/mean-absorption-time|Mean Absorption Time via Fundamental Matrix]] - row sums of $\mathbf{W}$.
- [[theorems/absorption-probabilities|Absorption Probabilities via Fundamental Matrix]] - $\mathbf{U}=\mathbf{W}\mathbf{R}$.

## Notation

- $P_{ij}$ for one-step transition probabilities.
- $P_{ij}^{(n)}$ for $n$-step transition probabilities.
- $\theta_{ij}$ for first passage time from $i$ to $j$.
- $\mathbf{Q}$ for transient-to-transient transition block.
- $\mathbf{R}$ for transient-to-absorbing transition block.

## Critique / Gaps

The chapter uses engineering examples heavily; this is useful for intuition, but some proofs rely on finite-state assumptions that must be revisited in Chapter 3 for countably infinite chains.

## Wiki Pages Updated

- [[concepts/markov-chain]], [[concepts/markov-property]], [[concepts/homogeneous-markov-chain]], [[concepts/initial-distribution]], [[concepts/transition-matrix]], [[concepts/n-step-transition-probability]], [[concepts/first-step-analysis]], [[concepts/first-passage-time]], [[concepts/absorbing-markov-chain]], [[concepts/fundamental-matrix]], [[concepts/random-walk]], [[concepts/m-g-1-queue]], [[concepts/g-m-1-queue]]
- [[theorems/markov-chain-factorization]], [[theorems/chapman-kolmogorov]], [[theorems/two-state-chain-n-step]], [[theorems/mean-first-passage-time]], [[theorems/fundamental-matrix]], [[theorems/mean-absorption-time]], [[theorems/absorption-probabilities]]
- [[topics/markov-chains]]
- [[exercises/markov-chain-joint-conditional-probabilities]], [[exercises/three-state-absorbing-chain]], [[exercises/four-state-absorbing-chain]], [[exercises/gambler-ruin]], [[exercises/layer-2-protocol-throughput]]
