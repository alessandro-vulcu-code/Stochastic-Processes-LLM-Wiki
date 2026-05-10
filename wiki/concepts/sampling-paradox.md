---
type: concept
tags: [stochastic-processes, renewal-process]
sources: [lecture-notes-ch5]
related: [[concepts/backward-recurrence-time]], [[concepts/excess-life]], [[concepts/renewal-process]]
---

# Sampling Paradox

**The sampling paradox is the bias that a random observation time is more likely to fall in a long renewal interval than in a short one.**

## Definition

In a renewal process, choosing a time $t$ independently of the renewal epochs does not sample a typical interrenewal interval. It samples an interval with probability proportional to its length.

## Key Properties

- The interval containing $t$ is length-biased.
- [[concepts/backward-recurrence-time|Backward Recurrence Time]] and [[concepts/excess-life|Excess Life]] reflect this bias.
- For non-exponential interrenewals, the residual life seen at a random time generally differs from the original interrenewal distribution.

## Intuition

If intervals are drawn on a line and you throw a dart at the line, long intervals occupy more space and are more likely to be hit.

## Connection to Other Concepts

This explains why $\mathbb{E}[S_{N(t)}]$ and $\mathbb{E}[S_{N(t)+1}]$ behave differently in renewal calculations.

## Theorems

- [[theorems/basic-renewal-theorem|Basic Renewal Theorem]]

## Examples

- Waiting at a random bus-stop time tends to put you inside a longer-than-average headway.

## Open Questions / Gaps

> [!todo] Gap - Add inspection paradox formulas for finite second moment cases.

## Sources

- [[sources/lecture-notes-ch5]] - sampling paradox and age/excess-life discussion.
