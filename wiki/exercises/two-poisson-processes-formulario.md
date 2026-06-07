---
type: exercise
tags: [exercise, exam-prep, poisson-process, conditional-probability]
sources: [two-poisson-processes-all, stochastic-exercises-guida-semplice, lecture-notes-ch4]
related: [poisson-process, superposition-theorem, two-processes-conditional-distribution, binomial-conditional-distribution, conditional-arrival-times-uniform]
---

# Formula Sheet - Two Poisson Processes

## Goal

Solve exam exercises with two independent Poisson processes $X_1(t),X_2(t)$ and conditional probabilities involving equal intervals, nested intervals, sums of processes, and partial information.

## Basic Notation

$$
X_i(t)=\#\text{ arrivals of process }i\text{ in }[0,t].
$$

To split intervals, use:

$$
N_i(a,b]=X_i(b)-X_i(a).
$$

Then:

$$
N_i(a,b]\sim\operatorname{Poisson}(\lambda_i(b-a)).
$$

Increments over disjoint intervals are independent. Different processes are independent.

## Poisson Formula

If $Y\sim\operatorname{Poisson}(\mu)$, then

$$
P(Y=k)=e^{-\mu}\frac{\mu^k}{k!}.
$$

Here:

$$
\mu=\lambda\cdot\text{interval length}.
$$

## Factorial Coefficients

Binomial formula without leaving $p$ as a separate placeholder. If one cell has mean $\mu_A$ and the conditioned total has mean $\mu_T$, then:

$$
P(Y=k)
=
\frac{n!}{k!(n-k)!}
\left(\frac{\mu_A}{\mu_T}\right)^k
\left(\frac{\mu_T-\mu_A}{\mu_T}\right)^{n-k},
\qquad k=0,\ldots,n.
$$

Multinomial formula. If the cells have means $\mu_1,\ldots,\mu_r$ and $\mu_T=\mu_1+\cdots+\mu_r$, then:

$$
P(Y_1=k_1,\ldots,Y_r=k_r)
=
\frac{n!}{k_1!\cdots k_r!}
\left(\frac{\mu_1}{\mu_T}\right)^{k_1}
\cdots
\left(\frac{\mu_r}{\mu_T}\right)^{k_r},
$$

with

$$
k_1+\cdots+k_r=n.
$$

## Universal Method

1. Draw one timeline for each process.
2. Split every count into disjoint cells, such as $N_1(0,1]$, $N_1(1,2]$, $N_2(0,2]$.
3. Assign each cell its mean $\mu=\lambda_i\Delta t$.
4. Rewrite the target event and the conditioning event using those cells.
5. If the condition and target do not overlap, use independence.
6. If the condition fixes a total, use binomial or multinomial splitting.
7. If counts overlap, subtract what is already known or use Bayes with a sum over possible cases.

## Case 1 - Two Processes, Same Interval

Type:

$$
P(X_1(t)=k\mid X_1(t)+X_2(t)=m).
$$

Complete formula:

$$
P(X_1(t)=k\mid X_1(t)+X_2(t)=m)
=
\frac{m!}{k!(m-k)!}
\left(\frac{\lambda_1}{\lambda_1+\lambda_2}\right)^k
\left(\frac{\lambda_2}{\lambda_1+\lambda_2}\right)^{m-k}.
$$

Version for $X_2$:

$$
P(X_2(t)=k\mid X_1(t)+X_2(t)=m)
=
\frac{m!}{k!(m-k)!}
\left(\frac{\lambda_2}{\lambda_1+\lambda_2}\right)^k
\left(\frac{\lambda_1}{\lambda_1+\lambda_2}\right)^{m-k}.
$$

## Case 2 - Total Given One Part

Type:

$$
P(X_1(t)+X_2(t)=m\mid X_1(t)=k).
$$

If $X_1(t)=k$ and the required total is $m$, then:

$$
X_2(t)=m-k.
$$

Thus:

$$
P(X_1(t)+X_2(t)=m\mid X_1(t)=k)
=
e^{-\lambda_2t}\frac{(\lambda_2t)^{m-k}}{(m-k)!},
\qquad m\ge k.
$$

If $m<k$, the probability is $0$.

## Case 3 - One Process, Subinterval Given Total

Type:

$$
P(X(s)=k\mid X(t)=m),\qquad 0<s<t.
$$

Given $m$ arrivals in $[0,t]$, each arrival falls in $[0,s]$ with probability $s/t$.

$$
P(X(s)=k\mid X(t)=m)
=
\frac{m!}{k!(m-k)!}\left(\frac{s}{t}\right)^k
\left(1-\frac{s}{t}\right)^{m-k}.
$$

## Case 4 - One Process On A Subinterval Given Two-Process Total

Type:

$$
P(X_1(s)=k\mid X_1(t)+X_2(t)=m),\qquad 0<s<t.
$$

Complete formula for $X_1(s)$:

$$
P(X_1(s)=k\mid X_1(t)+X_2(t)=m)
=
\frac{m!}{k!(m-k)!}
\left(\frac{\lambda_1s}{(\lambda_1+\lambda_2)t}\right)^k
\left(\frac{\lambda_1(t-s)+\lambda_2t}{(\lambda_1+\lambda_2)t}\right)^{m-k}.
$$

Complete formula for $X_2(s)$:

$$
P(X_2(s)=k\mid X_1(t)+X_2(t)=m)
=
\frac{m!}{k!(m-k)!}
\left(\frac{\lambda_2s}{(\lambda_1+\lambda_2)t}\right)^k
\left(\frac{\lambda_1t+\lambda_2(t-s)}{(\lambda_1+\lambda_2)t}\right)^{m-k}.
$$

## Case 5 - Future Total Given Partial Count

Type:

$$
P(X_1(t)+X_2(t)=m\mid X_1(s)=k),\qquad s<t.
$$

Split:

$$
X_1(t)=X_1(s)+[X_1(t)-X_1(s)].
$$

Given $X_1(s)=k$, the remaining $m-k$ arrivals must occur in the independent parts:

$$
[X_1(t)-X_1(s)]+X_2(t).
$$

That sum is Poisson with mean

$$
\lambda_1(t-s)+\lambda_2t.
$$

Thus:

$$
P(X_1(t)+X_2(t)=m\mid X_1(s)=k)
=
e^{-[\lambda_1(t-s)+\lambda_2t]}
\frac{[\lambda_1(t-s)+\lambda_2t]^{m-k}}{(m-k)!},
\qquad m\ge k.
$$

If $m<k$, the probability is $0$.

## Case 6 - Same Process With Nested Sum

Type:

$$
P(X(s)=a\mid X(s)+X(t)=m),\qquad s<t.
$$

Set:

$$
A=X(s),\qquad B=X(t)-X(s).
$$

Then $A$ and $B$ are independent, with

$$
A\sim\operatorname{Poisson}(\lambda s),
\qquad
B\sim\operatorname{Poisson}(\lambda(t-s)).
$$

The condition becomes:

$$
X(s)+X(t)=A+(A+B)=2A+B=m.
$$

Therefore:

$$
P(A=a\mid 2A+B=m)
=
\frac{P(A=a)P(B=m-2a)}
{\sum_{r=0}^{\lfloor m/2\rfloor}P(A=r)P(B=m-2r)}
$$

if $m-2a\ge0$; otherwise the probability is $0$.

Explicit formula:

$$
P(A=a\mid 2A+B=m)
=
\frac{
e^{-\lambda s}\frac{(\lambda s)^a}{a!}
e^{-\lambda(t-s)}\frac{[\lambda(t-s)]^{m-2a}}{(m-2a)!}
}
{
\sum_{r=0}^{\lfloor m/2\rfloor}
e^{-\lambda s}\frac{(\lambda s)^r}{r!}
e^{-\lambda(t-s)}\frac{[\lambda(t-s)]^{m-2r}}{(m-2r)!}
}.
$$

Reverse version:

$$
P(X(s)+X(t)=m\mid X(s)=a)
=
P(B=m-2a)
=
e^{-\lambda(t-s)}
\frac{[\lambda(t-s)]^{m-2a}}{(m-2a)!}.
$$

## Case 7 - Earlier Count Given Later Count

Type:

$$
P(X_1(s)+X_2(s)=m\mid X_1(t)=r),\qquad s<t.
$$

Given $X_1(t)=r$, the number of arrivals of $X_1$ in $[0,s]$ is:

$$
A=X_1(s)\mid X_1(t)=r\sim\operatorname{Binomial}\left(r,\frac{s}{t}\right).
$$

Also:

$$
B=X_2(s)\sim\operatorname{Poisson}(\lambda_2s),
$$

and $B$ is independent of $A$. Therefore:

$$
P(X_1(s)+X_2(s)=m\mid X_1(t)=r)
=
\sum_a
\frac{r!}{a!(r-a)!}
\left(\frac{s}{t}\right)^a\left(1-\frac{s}{t}\right)^{r-a}
e^{-\lambda_2s}\frac{(\lambda_2s)^{m-a}}{(m-a)!}.
$$

Sum only over possible values of $a$:

$$
0\le a\le r,\qquad 0\le m-a.
$$

## Case 8 - Condition That Implies Zero

If

$$
X_i(t)=0,
$$

then every subinterval inside $[0,t]$ has zero arrivals of the same process:

$$
X_i(s)=0,\qquad 0<s<t.
$$

Use this immediately to simplify. Do not run a long Bayes calculation when the condition already forces the result.

## Exam Examples

### Same Interval, Two Processes

With $\lambda_1=\lambda_2=1$:

$$
P(X_1(1)=1\mid X_1(1)+X_2(1)=2)
=
\frac{2!}{1!1!}\left(\frac12\right)^1\left(\frac12\right)^1
=\frac12.
$$

$$
P(X_1(1)+X_2(1)=2\mid X_1(1)=1)
=
P(X_2(1)=1)
=e^{-1}.
$$

### Subinterval Inside Two-Process Total

With $\lambda_1=\lambda_2=1$:

$$
P(X_1(1)=1\mid X_1(2)+X_2(2)=4).
$$

$$
\frac{4!}{1!3!}
\left(\frac{1\cdot1}{(1+1)\cdot2}\right)^1
\left(\frac{1(2-1)+1\cdot2}{(1+1)\cdot2}\right)^3
=\frac{27}{64}.
$$

### Future Total Given Partial Count

With $\lambda_1=\lambda_2=1$:

$$
P(X_1(2)+X_2(2)=4\mid X_1(1)=1).
$$

One arrival is already fixed. We need $3$ more arrivals in:

$$
X_1(2)-X_1(1)+X_2(2).
$$

Mean:

$$
1\cdot(2-1)+1\cdot2=3.
$$

Thus:

$$
e^{-3}\frac{3^3}{3!}
=\frac92e^{-3}.
$$

### Same Process With Nested Sum

With $\lambda_2=1$:

$$
P(X_2(1)=1\mid X_2(1)+X_2(2)=3).
$$

Set:

$$
A=X_2(1),\qquad B=X_2(2)-X_2(1).
$$

Condition:

$$
2A+B=3.
$$

Possible cases:

$$
(A,B)=(0,3),(1,1).
$$

Then:

$$
\frac{P(A=1)P(B=1)}
{P(A=0)P(B=3)+P(A=1)P(B=1)}
=
\frac{e^{-2}}{e^{-2}/6+e^{-2}}
=\frac67.
$$

Reverse:

$$
P(X_2(1)+X_2(2)=3\mid X_2(1)=1)
=P(B=1)=e^{-1}.
$$

### Earlier Count Given Later Count

With $\lambda_1=\lambda_2=1$:

$$
P(X_1(1)+X_2(1)=2\mid X_1(2)=1).
$$

Given $X_1(2)=1$, the unique arrival of $X_1$ falls in $[0,1]$ with probability $1/2$, or in $(1,2]$ with probability $1/2$.

Thus:

$$
\frac12P(X_2(1)=1)+\frac12P(X_2(1)=2)
=
\frac12e^{-1}+\frac12\frac{e^{-1}}2
=
\frac34e^{-1}.
$$

If instead

$$
P(X_1(1)+X_2(1)=2\mid X_1(2)=0),
$$

then $X_1(1)=0$, so we need $X_2(1)=2$:

$$
\frac{e^{-1}}2.
$$

## Final Checklist

- If you see $X_i(t)-X_i(s)$, it is an independent increment on $(s,t]$.
- If you see $X_i(s)$ inside $X_i(t)$, they are not independent: split into $A=X_i(s)$ and $B=X_i(t)-X_i(s)$.
- If the condition is a total, use binomial or multinomial splitting with probability equal to cell mean divided by total mean.
- If the condition already fixes a count, subtract that count from the required total.
- If an impossible case has positive-looking algebra, check constraints such as $m<k$ first.
- If stuck, return to the universal method: independent cells plus Bayes.

## Sources

- [[sources/two-poisson-processes-all]] - exam-prompt collection dedicated to this category.
- [[sources/stochastic-exercises-guida-semplice]] - operational solver/formula source.
- [[sources/lecture-notes-ch4]] - theoretical properties of Poisson processes.

