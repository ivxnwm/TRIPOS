# Numbers and sets

## Elementary number theory

**Theorem 1.1** Binomial theorem

**Theorem 1.2** Inclusion-exclusion principle

**Proposition 1.3**
> Every $n \in \mathbb{N}$ can be written as a product of primes.

**Theorem 1.4** infinitude of primes

**Proposition 1.5** Division algorithm

> Let $n, k \in \mathbb{N}$, then there exist unique $q, r \in \mathbb{N}$ such that $n = kq + r$ and $0 \leq r < k$.

**Theorem 1.6** Greatest common divisor
> The output of the Euclidean algorithm with input $a, b$ is $(a, b)$.

**Theorem 1.7** Bezout's identity
> $\forall a, b \in \mathbb{N}, \exists x, y \in \mathbb{Z}$ such that $xa + yb = (a, n)$.

**Corollary 1.8**
> Let $a, b \in \mathbb{N}$. Then the equation $ax + by = c$ has integer solutions if and only if $(a, b) \mid c$.

**Proposition 1.9** Euclid's lemma
> If a prime $p$ is prime and $p \mid ab$ then $p \mid a$ or $p \mid b$.
> 
> In general, if $p$ is prime and $p \mid a_1 a_2 \cdots a_n$ then $p \mid a_i$ for some $i$.

**Theorem 1.10** Fundamental theorem of arithmetic
> Every $n \in \mathbb{N}, n \ge 2$ is expressible as a product of primes uniquely up to reordering.

## Modular arithmetic

**Proposition 2.1**
> If $a$ is a unit $n$ then:
> * its inverse is unique
> * $ab \equiv ac \implies b \equiv c \mod n$ (this is not true in general for non-units).

**Proposition 2.2**
> Every $a \not\equiv 0 \mod p$ is a unit mod $p$ when $p$ is prime.

**Proposition 2.3**
> Let $n>2$, then $a$ is a unit mod $n$ if and only if $(a, n) = 1$.

**Corollary 2.4**
> If $(a,n) = 1$ then $ax \equiv b \mod n$ has a unique solution.

**Theorem 2.5** Chines remainder theorem
> Let $(m, n) = 1$, $a, b \in \mathbb{Z}$. Then the system of congruences $\begin{cases} x \equiv a \mod m \\ x \equiv b \mod n \end{cases}$ has a unique solution mod $mn$.
> 
> In general, if $m_1, m_2, \ldots, m_k$ are pairwise coprime, then $\forall a_1, a_2, \ldots, a_k \in \mathbb{Z}$, then the system of congruences $$\begin{cases} x \equiv a_1 \mod m_1 \\ x \equiv a_2 \mod m_2 \\ \vdots \\ x \equiv a_k \mod m_k \end{cases}$$ has a unique solution mod $m_1 m_2 \cdots m_k$.

**Definition 2.6** Euler's totient function
> $\varphi(n)$ is the number of integers $a$, $1 \leq a \leq n$, such that $(a, n) = 1$.

**Theorem 2.7** Fermat's little theorem
> If $p$ is prime and $p \nmid a$ then $a^{p-1} \equiv 1 \mod p$.

**Theorem 2.8** Fermat-Euler theorem
> If $(a, n) = 1$ then $a^{\varphi(n)} \equiv 1 \mod n$.

**Lemma 2.9**
> If $p$ is prime, then $x^2 \equiv 1 \mod p$ if and only if $x \equiv \pm 1 \mod p$.
> 
> In general, a nonzero polynomial of degree $d$ over $\mathbb{Z}_p$ has at most $d$ roots in $\mathbb{Z}_p$.

**Theorem 2.10** Wilson's theorem
> If $p$ is prime then $(p-1)! \equiv -1 \mod p$.

**Proposition 2.11**
> If p is an odd prime then -1 is a square mod p if and only if p ≡ 1 mod 4.

public key cryptography?

## Reals

Recall the construction of $\mathbb{N}$ using Peano axioms.

**Definition 3.1** Integers
> $\mathbb{Z}$ is the set of equivalence classes of $\mathbb{N} \times \mathbb{N}$ under the equivalence relation $(a, b) R (c, d) \iff a + d = b + c$.
> 
> Think of $(a, b)$ as $a - b$.
> 
> Write $0$ for $[(0, 0)]$, $-a$ for $[(1, 1+a)]$.
> 
> Define addition and multiplication as follows:
> * $[(a, b)] + [(c, d)] = [(a + c, b + d)]$
> * $[(a, b)] \cdot [(c, d)] = [(ac + bd, ad + bc)]$

**Definition 3.2** Rationals
> $\mathbb{Q}$ is the set of equivalence classes of $\mathbb{Z} \times \mathbb{n}$ under the equivalence relation $(a, b) R (c, d) \iff ad = bc$.
> 
> Write $\frac{a}{b}$ for $[(a, b)]$.
> 
> Define addition and multiplication as follows:
> * $[(a, b)] + [(c, d)] = [(ad + bc, bd)]$
> * $[(a, b)] \cdot [(c, d)] = [(ac, bd)]$
>
> Define an order on $\mathbb{Q}, <$ as follows:
> * if $a, b \in \mathbb{Q}$, then only one of $a < b$, $a = b$, $a > b$ holds.
> * if $a < b$ and $b < c$ then $a < c$.

**Poposition 3.3**
> $\nexists x \in \mathbb{Q}$ such that $x^2 = 2$.

**Proposition 3.4** (Key for defining reals)
> Let $A$ be the set of positive $a \in \mathbb{Q}$ such that $a^2 < 2$. Then $A$ contains no largest element.
> Similarly, the set $\{b \in \mathbb{Q}: b > 0, b^2 > 2\}$ contains no smallest element.

**Definition 3.5** Reals
> * $\mathbb{R}$ is a set with elements $0$ and $1$, $0 \neq 1$, equipped with operations $+$ and $\cdot$, and an ordering <, satisfying:
> * $\mathbb{R}$ is commutative and associative under $+$ with identity $0$, and every element has an inverse under $+$
> * $\mathbb{R}$ is commutative and associative under $\cdot$ with identity $1$, and every nonzero element has an inverse under $\cdot$
> * $\cdot$ is distributive over $+$: $\forall a, b, c \in \mathbb{R}, a \cdot (b + c) = a \cdot b + a \cdot c$
> * $\forall a, b, c \in \mathbb{R}$, exactly one of $a < b$, $a = b$, $a > b$ holds, and $a < b$ and $b < c \implies a < c$
> * $\forall a, b, c \in \mathbb{R}, a < b \implies a + c < b + c$, and if $c > 0$ $a < b \implies ac < bc$
> * Least upper bound axiom: given any set $S$ of reals that is nonempty and bounded above, $S$ has a least upper bound.

**Proposition 3.6** Axiom of Archimedes
> $\mathbb{N}$ is not bounded above in $\mathbb{R}$.

**Corollary 3.7**
> $\forall 0 < t \in \mathbb{R}, \exists n \in \mathbb{N}$ such that $\frac{1}{n} < t$.

**Theorem 3.8**
> $\exists x \in \mathbb{R}$ such that $x^2 = 2$.