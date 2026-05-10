---
type: exercise
tags: [exercise, markov-chains, stationary-distribution]
sources: [lecture-notes-ch4]
related: [markov-chain, stationary-distribution]
---

# Man with Car(s)

## Problem

A man travels between home and office. It rains independently on each trip with probability $p$. He drives if it is raining and a car is available at his current location; otherwise he walks. Find the long-run fraction of trips in which he walks in the rain with one car and with two cars.

## Solution

With one car, let $X_n=1$ if the car is available and $0$ otherwise. The stationary law is
$$
\pi_0=\frac{1-p}{2-p},\qquad \pi_1=\frac{1}{2-p}.
$$
The walking-in-rain fraction is
$$
\boxed{\frac{2p(1-p)}{2-p}}.
$$

With two cars, let $X_n$ be the number of cars at the current location. The stationary law is
$$
\pi_0=\frac{1-p}{3-p},\qquad
\pi_1=\frac{1}{3-p},\qquad
\pi_2=\frac{1}{3-p}.
$$
The fraction becomes
$$
\boxed{\frac{2p(1-p)}{3-p}}.
$$

## Concepts

- [[concepts/markov-chain|Markov Chain]]
- [[concepts/stationary-distribution|Stationary Distribution]]

## Sources

- [[sources/lecture-notes-ch4]]
