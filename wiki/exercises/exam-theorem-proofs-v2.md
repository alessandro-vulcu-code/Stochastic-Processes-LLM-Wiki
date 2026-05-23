---
type: exercise
tags: [exercise, exam-prep, markov-chains, poisson-process, renewal-process]
sources: [exams-theorems, lecture-notes-ch3, lecture-notes-ch4, lecture-notes-ch5]
related:
  - "[[theorems/finite-state-positive-recurrence]]"
  - "[[theorems/chapman-kolmogorov]]"
  - "[[theorems/elementary-renewal-theorem]]"
  - "[[theorems/period-class-property]]"
  - "[[theorems/binomial-conditional-distribution]]"
  - "[[theorems/poisson-interarrival-exponential]]"
  - "[[theorems/finiteness-renewal-function]]"
  - "[[theorems/solution-renewal-equation]]"
---

# Exam Theorem Proofs (v2)

Renewal-process notation: $X_1,X_2,\ldots$ are positive i.i.d. interarrival times, $\mu=\mathbb{E}[X_1]$, $S_n=X_1+\cdots+X_n$, $S_0=0$, $N(t)=\max\{n:S_n\leq t\}$, and $M(t)=\mathbb{E}[N(t)]$.

---

## 1. Finite Markov Chains Have No Null Recurrent States

>**Question**
>Prove that a Markov chain with a finite number of states cannot have any null recurrent state.

**Theorem.** A Markov chain with a finite state space cannot contain a null recurrent state.

**Proof.** Suppose $i$ is recurrent and let $C$ be its communicating class. First, $C$ is closed. Indeed, if some $j\notin C$ were reachable from $i$, then after reaching $j$ the chain could not return to $i$; otherwise $j$ would communicate with $i$ and would belong to $C$. This would give a positive probability of never returning to $i$, contradicting recurrence.

Thus $C$ is a finite closed irreducible Markov chain. Fix $i\in C$. For every $x\in C$, irreducibility gives a path from $x$ to $i$ with positive probability. Since $C$ is finite, we may take the minimum over all $x\in C$: choose $L<\infty$ as the longest such path and $\varepsilon>0$ as the smallest such probability, so that from every $x\in C$,
$$
\mathbb{P}_x(T_i\leq L)\geq \varepsilon,
$$
where $T_i=\inf\{n\geq 0:X_n=i\}$.

By the strong Markov property applied repeatedly at times $L,2L,\ldots$,
$$
\mathbb{P}_x(T_i>rL)\leq (1-\varepsilon)^r,\qquad r\geq 0.
$$
Hence
$$
\mathbb{E}_x[T_i]\leq \sum_{n=0}^\infty \mathbb{P}_x(T_i>n)\leq L\sum_{r=0}^\infty(1-\varepsilon)^r=\frac{L}{\varepsilon}<\infty.
$$
Starting from $i$, after one step the chain is still in $C$, so the first positive return time $T_i^+=\inf\{n\geq1:X_n=i\}$ has finite expectation. Therefore $i$ is positive recurrent. Since every recurrent state in a finite chain is positive recurrent, no recurrent state can be null recurrent. $\square$

---

## 2. Renewal Identity for $\mathbb{E}[S_{N(t)+1}]$

>**Question**
>Prove that for a renewal process $E[S_{N(t)+1}] = E[X](M(t) + 1)$.

**Theorem.** For a renewal process with finite mean $\mu=\mathbb{E}[X_1]$,
$$
\mathbb{E}[S_{N(t)+1}]=\mu(M(t)+1).
$$

**Proof.** Let $A(t)=\mathbb{E}[S_{N(t)+1}]$ be the expected epoch of the first renewal strictly after $t$. Condition on $X_1=x$.

If $x>t$, no renewal has occurred before $t$, so the next renewal epoch is $x$. If $x\leq t$, the process renews at time $x$ and restarts independently; the expected additional time to the first renewal after $t$ is $A(t-x)$. Therefore
$$
\mathbb{E}[S_{N(t)+1}\mid X_1=x]
=
\begin{cases}
x, & x>t,\\
x+A(t-x), & x\leq t.
\end{cases}
$$
Integrating with respect to $F$, the distribution of $X_1$,
$$
\begin{aligned}
A(t)
&=\int_{(0,t]} [x+A(t-x)]\,dF(x)+\int_{(t,\infty)} x\,dF(x)\\
&=\int_{(0,\infty)} x\,dF(x)+\int_{(0,t]} A(t-x)\,dF(x)\\
&=\mu+\int_{(0,t]} A(t-x)\,dF(x).
\end{aligned}
$$
This is a renewal equation with constant forcing term $\mu$. By [[theorems/solution-renewal-equation]], the solution of $Z(t)=a(t)+\int_0^t Z(t-x)\,dF(x)$ is $Z(t)=a(t)+\int_0^t a(t-x)\,dM(x)$. Here $a(t)=\mu$, so
$$
A(t)=\mu+\mu\int_0^t dM(x)=\mu(1+M(t)).
$$
Thus $\mathbb{E}[S_{N(t)+1}]=\mu(M(t)+1)$. $\square$

---

## 3. Chapman-Kolmogorov Equations

>**Question**
>Prove that for a Markov chain the $n$-step transition probabilities, $P_{ij}^{(n)}$, satisfy the relationship
   >$$P_{ij}^{(n)} = \sum_{m} P_{im}^{(k)} P_{mj}^{(n-k)}, k = 0, 1, \ldots, n$$

**Theorem.** For a homogeneous Markov chain and $0\leq k\leq n$,
$$
P_{ij}^{(n)}=\sum_m P_{im}^{(k)}P_{mj}^{(n-k)}.
$$

**Proof.** Decompose $\{X_n=j\}$ according to the intermediate state at time $k$:
$$
\begin{aligned}
P_{ij}^{(n)}
&=\mathbb{P}(X_n=j\mid X_0=i)\\
&=\sum_m \mathbb{P}(X_n=j,X_k=m\mid X_0=i)\\
&=\sum_m \mathbb{P}(X_k=m\mid X_0=i)\,\mathbb{P}(X_n=j\mid X_k=m,X_0=i).
\end{aligned}
$$
By the Markov property, conditional on $X_k=m$, the future is independent of the past. By homogeneity, the probability of moving from $m$ to $j$ in $n-k$ steps is $P_{mj}^{(n-k)}$. Hence
$$
P_{ij}^{(n)}=\sum_m P_{im}^{(k)}P_{mj}^{(n-k)}.
$$
For $k=0$ or $k=n$ the identity holds using $P^{(0)}=I$. In matrix form, $\mathbf{P}^{(n)}=\mathbf{P}^{(k)}\mathbf{P}^{(n-k)}=\mathbf{P}^n$. $\square$

---

## 4. Elementary Renewal Theorem

>**Question** 
>State and prove the elementary renewal theorem

**Theorem.** If $\mu=\mathbb{E}[X_1]\in(0,\infty)$, then
$$
\lim_{t\to\infty}\frac{M(t)}{t}=\frac{1}{\mu}.
$$

**Proof.** By [[theorems/finiteness-renewal-function]], $M(t)<\infty$ for all finite $t$, so the following manipulations are valid.

From Theorem 2,
$$
\mathbb{E}[S_{N(t)+1}]=\mu(M(t)+1).
$$
Since $S_{N(t)+1}>t$,
$$
t<\mu(M(t)+1),
$$
so
$$
\frac{M(t)}{t}>\frac{1}{\mu}-\frac{1}{t},
$$
and therefore
$$
\liminf_{t\to\infty}\frac{M(t)}{t}\geq \frac{1}{\mu}.
$$

For the upper bound, fix $a>0$ and define truncated interarrival times $Y_n=\min(X_n,a)$ with $\mu_a=\mathbb{E}[Y_1]$. Let $N_a(t)$ and $M_a(t)$ be the renewal count and renewal function for the $Y_n$-process. Since $Y_n\leq X_n$, truncated renewals occur no later than original ones, so $N(t)\leq N_a(t)$ and $M(t)\leq M_a(t)$. Also $Y_n\leq a$, so
$$
S^a_{N_a(t)+1}\leq t+a.
$$
Applying Theorem 2 to the truncated process:
$$
\mu_a(M_a(t)+1)=\mathbb{E}[S^a_{N_a(t)+1}]\leq t+a.
$$
Thus
$$
\frac{M(t)}{t}\leq\frac{M_a(t)}{t}\leq\frac{t+a}{\mu_a t}-\frac{1}{t},
$$
and
$$
\limsup_{t\to\infty}\frac{M(t)}{t}\leq \frac{1}{\mu_a}.
$$
Let $a\to\infty$. By monotone convergence, $\mu_a\uparrow\mu$, so
$$
\limsup_{t\to\infty}\frac{M(t)}{t}\leq \frac{1}{\mu}.
$$
Combining both bounds:
$$
\lim_{t\to\infty}\frac{M(t)}{t}=\frac{1}{\mu}.
$$
$\square$

---

## 5. Period Is a Class Property

>**Question** 
>Prove that in a Markov chain the period is a class property.

**Theorem.** If states $i$ and $j$ communicate, then they have the same period:
$$
i\leftrightarrow j\quad\Longrightarrow\quad d(i)=d(j).
$$

**Proof.** Let $S_i=\{s\geq1:P_{ii}^{(s)}>0\}$ and $d(i)=\gcd S_i$. Since $i\leftrightarrow j$, there exist $m,n\geq1$ such that $P_{ij}^{(m)}>0$ and $P_{ji}^{(n)}>0$.

Take any $s\in S_i$. Then $P_{ii}^{(s)}>0$. By joining paths $j\to i\to i\to j$:
$$
P_{jj}^{(n+s+m)}\geq P_{ji}^{(n)}P_{ii}^{(s)}P_{ij}^{(m)}>0,
$$
and repeating the $i\to i$ loop:
$$
P_{jj}^{(n+2s+m)}>0.
$$
Since every element of $S_j$ is divisible by $d(j)$,
$$
n+s+m=k_1d(j),\qquad n+2s+m=k_2d(j).
$$
Subtracting: $s=(k_2-k_1)d(j)$. So every $s\in S_i$ is divisible by $d(j)$, meaning $d(j)\mid d(i)$. Reversing the roles of $i$ and $j$ gives $d(i)\mid d(j)$. Hence $d(i)=d(j)$. $\square$

---

## 6. Conditional Poisson Count in a Subinterval

> **Question** 
> Prove that for a Poisson process $X(t)$ the statistics of $X(s)$ conditioned on $X(t), s < t$, is binomial, and provide the expression of $P[X(s) = k|X(t) = n]$.

**Theorem.** Let $X(t)$ be a Poisson process of rate $\lambda$. If $0<s<t$ and $0\leq k\leq n$, then
$$
\mathbb{P}[X(s)=k\mid X(t)=n]
=
\binom{n}{k}\left(\frac{s}{t}\right)^k
\left(1-\frac{s}{t}\right)^{n-k}.
$$

**Proof.** Since $X(t)=X(s)+[X(t)-X(s)]$ and Poisson increments over disjoint intervals are independent,
$$
\begin{aligned}
\mathbb{P}[X(s)=k\mid X(t)=n]
&=\frac{\mathbb{P}[X(s)=k,\ X(t)-X(s)=n-k]}{\mathbb{P}[X(t)=n]}\\
&=\frac{
e^{-\lambda s}\frac{(\lambda s)^k}{k!}\cdot
e^{-\lambda(t-s)}\frac{(\lambda(t-s))^{n-k}}{(n-k)!}
}{
e^{-\lambda t}\frac{(\lambda t)^n}{n!}
}\\
&=\binom{n}{k}\left(\frac{s}{t}\right)^k
\left(\frac{t-s}{t}\right)^{n-k}.
\end{aligned}
$$
This is the $\mathrm{Binomial}(n,s/t)$ probability mass function. $\square$

---

## 7. Recurrence Is a Class Property

>**Question** 
>Prove that if states $i$ and $j$ of a Markov chain communicate and $i$ is recurrent, then $j$ is also recurrent.

**Theorem.** If states $i$ and $j$ communicate and $i$ is recurrent, then $j$ is recurrent.

**Proof.** Since $i\leftrightarrow j$, there exist $m,n\geq1$ such that $P_{ji}^{(m)}>0$ and $P_{ij}^{(n)}>0$. For every $\nu\geq0$,
$$
P_{jj}^{(m+\nu+n)}
\geq
P_{ji}^{(m)}P_{ii}^{(\nu)}P_{ij}^{(n)}.
$$
Summing over $\nu$:
$$
\sum_{\nu=0}^{\infty}P_{jj}^{(m+\nu+n)}
\geq
P_{ji}^{(m)}P_{ij}^{(n)}
\sum_{\nu=0}^{\infty}P_{ii}^{(\nu)}.
$$
Since $i$ is recurrent, $\sum_{\nu=0}^{\infty}P_{ii}^{(\nu)}=\infty$ by [[theorems/recurrence-criterion]]. The constants $P_{ji}^{(m)},P_{ij}^{(n)}>0$, so the left-hand series diverges:
$$
\sum_{\ell=0}^{\infty}P_{jj}^{(\ell)}=\infty.
$$
By the same criterion, $j$ is recurrent. $\square$

---

## 8. Poisson Interarrival Times Are I.I.D. Exponential

> **Question** 
> For a Poisson process of rate $\lambda$, prove that the interarrival times are iid exponential with mean $1/\lambda$.

**Theorem.** For a Poisson process of rate $\lambda$, the interarrival times are i.i.d. exponential random variables with mean $1/\lambda$.

**Proof.** Write $\tau_n$ for the $n$-th interarrival time and $W_n=\tau_1+\cdots+\tau_n$ for the $n$-th arrival epoch (using $\tau,W$ here to avoid confusion with the renewal notation $X_n,S_n$ in the preamble).

Let $\tau_1$ be the time to the first arrival. Then
$$
\mathbb{P}(\tau_1>t)=\mathbb{P}(X(t)=0)=e^{-\lambda t},
$$
so $\tau_1\sim\mathrm{Exp}(\lambda)$.

Conditional on the history up to $W_n$, the waiting time until the next arrival exceeds $t$ exactly when there are no arrivals in $(W_n,W_n+t]$. Since $W_n$ is a stopping time, the strong Markov property of the Poisson process gives a fresh Poisson process after $W_n$; by stationary increments,
$$
\mathbb{P}(\tau_{n+1}>t\mid\text{history up to }W_n)
=\mathbb{P}(X(t)=0)=e^{-\lambda t}.
$$
Thus every interarrival time has exponential distribution with rate $\lambda$, and each is independent of the past. Hence $\tau_1,\tau_2,\ldots$ are i.i.d. $\mathrm{Exp}(\lambda)$, with mean
$$
\mathbb{E}[\tau_n]=\int_0^\infty e^{-\lambda t}\,dt=\frac{1}{\lambda}.
$$
$\square$

---

## 9. Reflected Random Walk on Non-Negative Integers

> **Question** 
> Consider a random walk over the non-negative integers with the following transition probabilities:
>    $$P_{01} = 1, P_{i,i+1} = p, P_{i,i-1} = q, i > 0, \text{ with } p + q = 1.$$ Study its behavior, and in particular characterize its recurrence or transience and derive the steady-state distribution.
> 

**Theorem.** Consider the Markov chain on $\mathbb{N}$ with
$$
P_{01}=1,\qquad P_{i,i+1}=p,\qquad P_{i,i-1}=q,\quad i>0,\qquad p+q=1,
$$
and $0<p,q<1$. Then:

- if $p<q$: chain is positive recurrent;
- if $p=q=1/2$: chain is null recurrent;
- if $p>q$: chain is transient.

When $p<q$, the stationary distribution is
$$
\pi_0=\frac{q-p}{1+q-p}=\frac{q-p}{2q},
\qquad
\pi_i=\pi_0\frac{p^{i-1}}{q^i},\quad i\geq1.
$$

**Proof.** *Recurrence/transience.* Let $h_i=\mathbb{P}_i(T_0<\infty)$. Then $h_0=1$ and for $i\geq1$:
$$
h_i=ph_{i+1}+qh_{i-1}.
$$
General solution:
$$
h_i=
\begin{cases}
A+B(q/p)^i, & p\neq q,\\
A+Bi, & p=q.
\end{cases}
$$
Using $h_0=1$ and $0\leq h_i\leq1$:

- $p<q$: $(q/p)^i\to\infty$, so boundedness forces $B=0$, giving $h_i=1$ (recurrent).
- $p=q$: boundedness forces $B=0$, giving $h_i=1$ (recurrent).
- $p>q$: set $r=q/p<1$. To identify the relevant bounded solution, first stop the chain on $\{0,\ldots,R\}$ and let $h_i^{(R)}=\mathbb{P}_i(T_0<T_R)$. Solving the same difference equation with $h_0^{(R)}=1$ and $h_R^{(R)}=0$ gives
  $$
  h_i^{(R)}=\frac{r^i-r^R}{1-r^R}.
  $$
  Letting $R\to\infty$ gives $h_i=r^i=(q/p)^i<1$ (transient).

*Stationary distribution.* Birth-death detailed balance gives $\pi_0P_{01}=\pi_1P_{10}$ and $\pi_iP_{i,i+1}=\pi_{i+1}P_{i+1,i}$ for $i\geq1$, so:
$$
\pi_1=\frac{\pi_0}{q},\qquad \pi_{i+1}=\frac{p}{q}\pi_i,
$$
yielding $\pi_i=\pi_0 p^{i-1}/q^i$ for $i\geq1$. Normalization:
$$
1=\pi_0\left[1+\frac{1}{q}\sum_{i=1}^{\infty}\left(\frac{p}{q}\right)^{i-1}\right]
=\pi_0\left(1+\frac{1}{q-p}\right)
=\pi_0\frac{1+q-p}{q-p}.
$$
The geometric series converges iff $p<q$. Since $p+q=1$, we have $1+q-p=2q$, so $\pi_0=(q-p)/(2q)$.

*Classification summary.* For $p<q$: normalizable stationary distribution exists, so positive recurrent. For $p=q$: recurrent but no normalizable $\pi$ (geometric series diverges), so null recurrent. For $p>q$: transient.

*Period.* From state 0, all transitions go to state 1 first ($P_{01}=1$), and from any state $i\geq1$ transitions change the index by $\pm1$. Every return to any state therefore requires an even number of steps, so the chain has period 2 for all states (period is a class property by [[theorems/period-class-property]]). Consequently $\pi$ gives long-run time proportions, not one-step limiting probabilities; one-step limits $P_{ii}^{(n)}$ oscillate by parity of $n$ and do not converge to $\pi_i$ directly. $\square$

---

## 10. Formal Renewal Identity for $\mathbb{E}[S_{N(t)+1}]$ via Wald's Equation

> **Question** 
> For a renewal process, give an expression for $E[S_{N(t)+1}]$, also providing a formal proof.

**Theorem.** For a renewal process with $\mu=\mathbb{E}[X_1]<\infty$,
$$
\mathbb{E}[S_{N(t)+1}]=\mathbb{E}[X_1](M(t)+1).
$$

**Proof.** By [[theorems/finiteness-renewal-function]], $M(t)<\infty$ for all finite $t$. Let
$$
T=N(t)+1=\min\{n\geq1:S_n>t\}.
$$
With respect to $\mathcal{F}_n=\sigma(X_1,\ldots,X_n)$, $T$ is a stopping time because
$$
\{T\leq n\}=\{N(t)+1\leq n\}=\{N(t)\leq n-1\}=\{S_n>t\}\in\mathcal{F}_n.
$$
Also $T<\infty$ a.s. and
$$
\mathbb{E}[T]=M(t)+1<\infty.
$$
By Wald's first equation (i.i.d. nonnegative $X_r$ with finite mean, stopping time $T$ with finite mean):
$$
\mathbb{E}[S_T]=\mathbb{E}[T]\,\mathbb{E}[X_1]=(M(t)+1)\,\mathbb{E}[X_1].
$$
Since $T=N(t)+1$ and $S_T=S_{N(t)+1}$:
$$
\mathbb{E}[S_{N(t)+1}]=\mathbb{E}[X_1](M(t)+1).
$$
$\square$

---

## 11. Conditional Poisson Counts: Smaller and Larger Time Horizons

> **Question** 
> For a Poisson process $X(t)$ of rate $\lambda$, state and derive the expression of $P[X(u) = k|X(t) = n]$ for the two cases (i) $0 < u < t, 0 \leq k \leq n$ and (ii) $0 < t < u, 0 \leq n \leq k$.

**Theorem.** Let $X(t)$ be a Poisson process of rate $\lambda$.

For $0<u<t$ and $0\leq k\leq n$:
$$
\mathbb{P}[X(u)=k\mid X(t)=n]
=
\binom{n}{k}\left(\frac{u}{t}\right)^k
\left(1-\frac{u}{t}\right)^{n-k}.
$$

For $0<t<u$ and $0\leq n\leq k$:
$$
\mathbb{P}[X(u)=k\mid X(t)=n]
=
e^{-\lambda(u-t)}
\frac{[\lambda(u-t)]^{k-n}}{(k-n)!}.
$$

**Proof.** *Case (i): $0<u<t$.* This is Theorem 6 with $s=u$. By independence of Poisson increments:
$$
\mathbb{P}[X(u)=k\mid X(t)=n]
=\frac{\mathbb{P}[X(u)=k,\ X(t)-X(u)=n-k]}{\mathbb{P}[X(t)=n]}
=\binom{n}{k}\left(\frac{u}{t}\right)^k\left(\frac{t-u}{t}\right)^{n-k}.
$$

*Case (ii): $0<t<u$.* Conditioning on $X(t)=n$ and using the Markov property of the Poisson process, $X(u)-X(t)$ is independent of $X(t)$ with distribution $\mathrm{Poisson}(\lambda(u-t))$:
$$
\begin{aligned}
\mathbb{P}[X(u)=k\mid X(t)=n]
&=\mathbb{P}[X(u)-X(t)=k-n\mid X(t)=n]\\
&=\mathbb{P}[X(u)-X(t)=k-n]\\
&=e^{-\lambda(u-t)}\frac{[\lambda(u-t)]^{k-n}}{(k-n)!}.
\end{aligned}
$$
If $k<n$ the probability is $0$. $\square$

---

## 12. Almost-Sure Renewal Rate

>**Question** 
>For a renewal process, state precisely (also providing a formal proof) what is the value of
   >$$\lim_{t \to \infty} \frac{N(t)}{t}$$

**Theorem.** If $\mu=\mathbb{E}[X_1]\in(0,\infty)$, then
$$
\lim_{t\to\infty}\frac{N(t)}{t}=\frac{1}{\mu}
\qquad\text{almost surely.}
$$

**Proof.** Since interarrival times are positive and finite, $S_n\to\infty$ a.s., hence $N(t)\to\infty$ as $t\to\infty$. By definition of $N(t)$:
$$
S_{N(t)}\leq t<S_{N(t)+1}.
$$
For $N(t)>0$, divide by $N(t)$:
$$
\frac{S_{N(t)}}{N(t)}
\leq
\frac{t}{N(t)}
<
\frac{S_{N(t)+1}}{N(t)}
=
\frac{S_{N(t)+1}}{N(t)+1}\cdot\frac{N(t)+1}{N(t)}.
$$
As $t\to\infty$, $N(t)\to\infty$. By the strong law of large numbers applied along the random index $N(t)$:
$$
\frac{S_{N(t)}}{N(t)}\to\mu,
\qquad
\frac{S_{N(t)+1}}{N(t)+1}\to\mu
\qquad\text{a.s.}
$$
Also $(N(t)+1)/N(t)\to1$. The squeeze theorem gives $t/N(t)\to\mu$ a.s., and taking reciprocals:
$$
\frac{N(t)}{t}\to\frac{1}{\mu}
\qquad\text{a.s.}
$$
$\square$

---

## Source Links

- [[sources/exams-theorems|Exams Theorems]]
- [[sources/lecture-notes-ch3|Chapter 3 - Long Run Behaviour of Markov Chains]]
- [[sources/lecture-notes-ch4|Chapter 4 - Poisson Processes]]
- [[sources/lecture-notes-ch5|Chapter 5 - Renewal Phenomena]]
