---
type: topic
tags: [gobackn, semi-markov-processes, renewal-reward]
sources: [lecture-notes-ch6]
---

# GoBackN Protocol Analysis

## Overview

GoBackN is analyzed as a semi-Markov reward process. The protocol skips slots after errors, so throughput is not just the fraction of good channel states; it is successful accepted packets divided by real slots consumed.

## Core Concepts

- [[concepts/gobackn-protocol|GoBackN Protocol]]
- [[concepts/semi-markov-process|Semi-Markov Process]]
- [[concepts/renewal-reward-process|Renewal Reward Process]]
- [[concepts/transition-generating-matrix|Transition Generating Matrix]]

## Key Theorems

- [[theorems/gobackn-throughput-markov-errors|GoBackN Throughput with Markov Errors]]
- [[theorems/transition-generating-matrix-method|Transition Generating Matrix Method]]

## Suggested Reading Order

1. [[sources/lecture-notes-ch6]]
2. [[concepts/gobackn-protocol]]
3. [[theorems/gobackn-throughput-markov-errors]]
4. [[concepts/transition-generating-matrix]]
5. [[exercises/gobackn-transform-throughput]]

## Open Problems / Active Research

> [!todo] Gap - Reconstruct OCR-damaged transition matrices into clean LaTeX if this protocol becomes exam-critical.

