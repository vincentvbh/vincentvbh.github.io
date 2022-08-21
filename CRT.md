
# Chinese Remainder Theorem for Rings

This page explains the Chinese remainder theorem for rings (with identity) and is largely based on the Proposition 10 in <cite>[Bou89, Chapter I, Section 8]</cite>.

## Objectives
Let $R$ be a ring, $\calI = \set{0, \dots, m - 1}$ be an index set, and $(I_i)\_{i \in \calI}$ be a system of pair-wise coprime ideals.
- Then, we have an isomorphism $\eta$ for
    \\[
    \frac{R}{\bigcap_{i \in \calI} I_i} \cong \prod_{i \in \calI} \frac{R}{I_i}
    \\]
    by sending $x \bmod \bigcap_{i \in \calI} I_i$ to $(x \bmod I_i)\_{i \in \calI}$.
- If $\bigcap_{i \in \calI} I_i = 0$, we have $\exists e_{\calI} \in R^m, \forall i \in \calI, I_i = (1 - e_i) R$ where
    $e_{\calI}$ is a system of pair-wise orthogonal central idempotent elements.
- $\eta^{-1}$ is the map $x_{\calI} \mapsto \sum_{i \in \calI} e_i x_i$.
- The existence of $e_{\calI}$ is equivalent to the existence of $I_{\calI}$ with $\bigcap_{i \in \calI} I_i = 0$.

## Coprime Ideals

### Definitions
- Coprime ideals $I_0$ and $I_1$ of the ring $R$.
    \\[
    \exists r_0 \in I_0, \exists r_1 \in I_1, r_0 + r_1 = 1.
    \\]
    Equivalently,
    \\[
    I_0 + I_1 = R.
    \\]
- A system of pair-wise coprime ideals $I_{\calI}$.
    \\[
    \forall i, j \in \calI, i \neq j \implies I_i + I_j = R.
    \\]

### Case of two coprime ideals

Let $R$ be a ring, and $I_0$ and $I_1$ be ideals of $R$.
We say that $I_0$ and $I_1$ are coprime if there are elements $r_0 \in I_0$ and $r_1 \in I_1$ such that $r_0 + r_1 = 1$.
This is equivalent to $I_0 + I_1 = R$.
The Chinese remainder theorem states that there is an isomorphism $\eta$ from $\frac{R}{I_0 \cap I_1}$ to $\frac{R}{I_0} \times \frac{R}{I_1}$ sending
$x \bmod I_0 \cap I_1$ to $(x \bmod I_0, x \bmod I_1)$.

### Case of finitely many pair-wise coprime ideals

We can generalize it to ideals that are pair-wise coprime.
The ideals $I_0, \dots, I_m$ are called pair-wise coprime if for $i \neq j$, $I_i$ and $I_j$ are coprime.
Let $I_{\calI}$ be a system of pair-wise coprime ideals.
The Chinese remainder theorem states that there is an isomorphism $\eta$ from $\frac{R}{\bigcap_{i \in \calI} I_i}$ to $\prod_{i \in \calI} I_i$ sending
$x \bmod \bigcap_{i \in \calI} I_i$ to $(x \bmod I_i)\_{i \in \calI}$.

### Examples

TBA

## Idempotent Elements

### Definitions

- Idempotent element $e \in R$.
    \\[
    e^2 = e.
    \\]
- A system of orthogonal idempotent elements $e_{\calI} \in R^m$.
    \\[
    \forall i, j \in \calI, e_i e_j = \delta_{i, j} e_i.
    \\]

In a ring $R$, an element $e$ is called idempotent if $e^2 = e$.
Furthermore, if $e$ commutes with all the elements of $R$, we call it a central idempotent element.
Let $e_1$ and $e_2$ be two distinct idempotent elements in $R$.
They are called orthogonal if $e_1 e_2 = e_2 e_1 = 0$.
The Chinese remainder theorem for rings is closely related to a system of pair-wise orthogonal central idempotent elements that sums to $1$.

### Case of two orthogonal central idempotent elements

Let $e_0, e_1 \in R$ be two orthogonal central idempotent elements with $e_0 + e_1 = 1$ and define $I_0 = (1 - e_0) R$ and $I_1 = (1 - e_1) R$.
We claim the following.
- $I_0$ and $I_1$ are coprime.
- $I_0 \cap I_1 = \set{0}$.

For showing $I_0 \cap I_1 = \set{0}$, we will prove the following observations.
- $I_0 I_1 =  I_0 \cap I_1$.
- $I_0 I_1 = \set{0}$.

Clearly, if the observations hold, we have $I_0 \cap I_1 = \set{0}$.

#### Proofs

- Prove that $I_0$ and $I_1$ are coprime.
    - Since $e_2 \in e_2 R = I_0$, $e_1 \in e_1 R = I_1$, and $e_2 + e_1 = 1$,
    $I_0$ and $I_1$ are coprime as desired.

- Proof for $I_0 I_1 =  I_0 \cap I_1$.
    - We first recall that for two coprime ideals $J$ and $K$, $J \cap K = J K + K J$.
    For the proof, please refer to the supplementary material.
    Once we show that $I_0 I_1 = I_1 I_0$, we prove the observation.
    For arbitrary $r_{0, 0}$, $\dots$, $r_{0, c - 1}$, $r_{1, 0}$, $\dots$, $r_{1, c - 1} \in R$,
    since $\sum_{i = 0}^{c - 1} (1 - e_0) r_{0, i} (1 - e_1) r_{1, i} = \sum_{i = 0}^{c - 1} (1 - e_1) r_{0, i} (1 - e_0) r_{1, i}$,
    we have $I_0 I_1 = I_1 I_0$ as desired.

- Proof for $I_0 I_1 = \set{0}$.
    - Since for arbitrary $r_0, r_1 \in R$, $(1 - e_0) r_0 (1 - e_1) r_1 = (1 - (e_0 + e_1)) r_0 r_1 = 0$, we have for arbitrary $r_{0, 0}, \dots, r_{0, c - 1}, r_{1, 0}, \dots, r_{1, c - 1} \in R$, $\sum_{i = 0}^{c - 1} (1 - e_0) r_{0, i} (1 - e_1) r_{1, i} = 0$.
    Therefore, $I_0 I_1 = \set{ \sum_{i = 0}^{c - 1} (1 - e_0) r_{0, i} (1 - e_1) r_{1, i} | r_0, r_1 \in R, c \in \mN^+} = \set{0}$ as desired.

### Case of finitely many orthogonal central idempotent elements

We generalize to $e_\calI$ as follows. Let's write $I_i$ for $(1 - e_i) R$.
- For $i \neq j$, the ideals $I_i$ and $I_j$ are coprime.
- $\bigcap_{i \in \calI} I_i = \set{0}$.

Similarly, for showing $\bigcap_{i \in \calI} I_i = \set{0}$, we will prove the following.
- $\prod_{i \in \calI} I_i = \bigcap_{i \in \calI} I_i$.
- $\prod_{i \in \calI} I_i = \set{0}$.



#### Proofs

- Prove that for $i \neq j$, the ideals $I_i$ and $I_j$ are coprime.
    - We first observe that $e_i = (1 - e_j) e_i \in I_j $.
        Now, we choose $1 - e_i \in (1 - e_i) R$ and $e_i \in (1 - e_j) R$ which sums to $1$ as desired.
- Proof for $\prod_{i \in \calI} (1 - e_i) R = \bigcap_{i \in \calI} (1 - e_i) R$.
    - We proceed similarly by first recalling $\bigcap_{i \in \calI} J_i = \sum_{\pi \in S_m} \prod_{i \in \calI} J_{\pi(i)}$ for mutually coprime ideals $J_\calI$.
        The proof is given as a supplementary material.
        We now claim that for arbitrary $\pi_1, \pi_2 \in S_m$, $\prod_{i \in \calI} (1 - e_{\pi_1(i)}) R = \prod_{i \in \calI} (1 - e_{\pi_1(i)}) R$.
        This is immediate since we know that for $i \neq j$, $\left( (1 - e_i) R \right) \left( (1 - e_j) R \right) = \left( (1 - e_j) R \right) \left( (1 - e_i) R \right)$.
        We conclude that $\bigcap_{i \in \calI} (1 - e_i) R = \sum_{\pi \in S_m} \prod_{i \in \calI} (1 - e_{\pi(i)}) R = \prod_{i \in \calI} (1 - e_i) R$.
- Proof for $\prod_{i \in \calI} (1 - e_i) R = \set{0}$.
    - For arbitrary $r_\calI \in R^m$, we claim that $\prod_{i \in \calI} (1 - e_i) r_i = 0$.
        Once we show this, we have 
        \\[
        \prod_{i \in \calI} (1 - e_i) R = \set{ \prod_{i \in \calI} (1 - e_i) r_i | r_\calI \in R^m } = \set{0}
        \\]
        as desired.
        We show $\prod_{i \in \calI} (1 - e_i) r_i = 0$ as follows.
        \\[
        \prod_{i \in \calI} (1 - e_i) r_i = \left( \prod_{i \in \calI} (1 - e_i) \right) \left( \prod_{i \in \calI} r_i \right) = \left( 1 - \sum_{i \in \calI} e_i \right) \left( \prod_{i \in \calI} r_i \right) = 0.
        \\]

### Examples

TBA

# Supplementary

- Let $I_\calI$ be pair-wise coprime ideals of $R$. We have
    \\[
    \bigcap_{i \in \calI} I_i = \sum_{\pi \in S_m} \prod_{i \in \calI} I_{\pi(i)}
    \\]
    where $S_m$ is the symmetric group defined on a set of $m$ elements.
    Since $\sum_{\pi \in S_m} \prod_{i \in \calI} I_{\pi(i)} \subseteq \bigcap_{i \in \calI} I_i$ by the definition of ideals, we only need to show $\bigcap_{i \in \calI} I_i \subseteq \sum_{\pi \in S_m} \prod_{i \in \calI} I_{\pi(i)}$.
    We prove by induction on $m$ as follows.
    - $m = 2$: since there are elements $r_0 \in I_0$ and $r_1 \in I_1$ with $r_0 + r_1 = 1$, 
        we write an element $x \in I_0 \cap I_1$ as $x = x(r_0 + r_1) = x r_0 + x r_1 \in I_1 I_0 + I_0 I_1$, and therefore $I_0 \cap I_1 \subseteq I_0 I_1 + I_1 I_0$.
    - $m \implies m + 1$: 
    \\[
    \bigcap_{i \in \set{0, \dots, m}} I_i \subseteq \left( \sum_{\pi \in S_m} \prod_{i \in \set{0, \dots, m - 1}} I_{\pi(i)} \right) I_m + I_m \left( \sum_{\pi \in S_m} \prod_{i \in \set{0, \dots, m - 1}} I_{\pi(i)} \right) \subseteq \sum_{\pi \in S_{m + 1}} \prod_{i \in \set{0, \dots, m}} I_{\pi(i)}.
    \\]

# References
- <cite>[Bou89]</cite> Algebra. Nicolas Bourbaki. 1989.











