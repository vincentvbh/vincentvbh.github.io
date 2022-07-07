
# Chinese Remainder Theorem for Rings

This page explains the Chinese remainder theorem for rings.

## Objectives
Let $R$ be a ring, $\calI = \set{0, \dots, m - 1}$ be an index set, and $(I_i)\_{i \in \calI}$ be a system of pair-wise coprime ideals.
- Then, we have an isomorphism $\eta$ for
    \\[
    \frac{R}{\bigcap_{i \in \calI} I_i} \cong \prod_{i \in \calI} \frac{R}{I_i}.
    \\]
- $\eta$ is the map $x \bmod \bigcap_{i \in \calI} I_i \mapsto (x \bmod I_i)\_{i \in \calI}$.
- $\exists e_{\calI}, \forall i \in \calI, I_i = (1 - e_i) R$ where
    $e_{\calI}$ is a system of pair-wise orthogonal central idempotent elements.
- $\eta^{-1}$ is the map $x_{\calI} \mapsto \sum_{i \in \calI} e_i x_i$.
- The existence of $e_{\calI}$ is equivalent to the existence of $I_{\calI}$ with $\bigcap_{i \in \calI} I_i = 0$.

## Coprime Ideals

### Definitions
- Coprime ideals $I_1$ and $I_2$ of the ring $R$.
    \\[
    \exists i_1 \in I_1, \exists i_2 \in I_2, i_1 + i_2 = 1.
    \\]
    Equivalently,
    \\[
    I_1 + I_2 = R.
    \\]
- A system of pair-wise coprime ideals $I_{\calI}$.
    \\[
    \forall i, j \in \calI, i \neq j \implies I_i + I_j = R.
    \\]

### Contents

Let $R$ be a ring, and $I_1$ and $I_2$ be ideals of $R$.
We say that $I_1$ and $I_2$ are coprime if there are elements $i_1 \in I_1$ and $i_2 \in I_2$ such that $i_1 + i_2 = 1$.
This is equivalent to $I_1 + I_2 = R$.
The Chinese remainder theorem states that there is an isomorphism $\eta$ from $\frac{R}{I_1 \cap I_2}$ to $\frac{R}{I_1} \times \frac{R}{I_2}$ sending
$x \bmod I_1 \cap I_2$ to $(x \bmod I_1, x \bmod I_2)$.

We can generalize it to ideals that are pair-wise coprime.
The ideals $I_1, \dots, I_m$ are called pair-wise coprime if for $i \neq j$, $I_i$ and $I_j$ are coprime.
Let $I_{\calI}$ be a system of pair-wise coprime ideals.
The Chinese remainder theorem states that there is an isomorphism $\eta$ from $\frac{R}{\bigcap_{i \in \calI} I_i}$ to $\prod_{i \in \calI} I_i$ sending
$x \bmod \bigcap_{i \in \calI} I_i$ to $(x \bmod I_i)\_{i \in \calI}$.

### Examples

## Idempotent Elements

### Definitions

- Idempotent element $e$.
    \\[
    e^2 = e.
    \\]
- A system of orthogonal idempotent elements $e_{\calI}$.
    \\[
    \forall i, j \in \calI, e_i e_j = \delta_{i, j} e_i.
    \\]

### Contents

In a ring, an element $e$ is called idempotent if $e^2 = e$.
Furthermore, if $e$ commutes with all the elements of $R$, we call it a central idempotent element.
Let $e_1$ and $e_2$ be two distinct idempotent elements in $R$.
They are called orthogonal if $e_1 e_2 = e_2 e_1 = 0$.
The Chinese remainder theorem for rings is closely related to a system of pair-wise orthogonal central idempotent elements that sums to $1$.
We first illustrate the idea where two orthogonal central idempotent elements are involved.

Given two orthogonal central idempotent elements $e_1$ and $e_2$ in $R$ with $e_1 + e_2 = 1$,
we claim that the ideals $(1 - e_1) R$ and $(1 - e_2) R$ are coprime.
In other words, there are elements $i_1 \in (1 - e_1) R$ and $i_2 \in (1 - e_2) R$ such that
$i_1 + i_2 = 1$ in $R$.
We choose $i_1 = e_1$ and $i_2 = e_2$.
Since $e_1 + e_2 = 1$, it remains to verify that $e_2 \in (1 - e_1) R$ and $e_1 \in (1 - e_2) R$.
This is immediate since $1 = e_1 + e_2$ tells us that $e_2 \in e_2 R = (1 - e_1) R$ and $e_1 \in e_1 R = (1 - e_2) R$.

### Examples











