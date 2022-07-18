
# Good--Thomas Fast Fourier Transform

## Objectives
Let $R$ be a ring, $\calD = \set{0, \dots, d - 1 }$ be an index set, $q_\calD$ be $d$ coprime integers, $\calQ = \prod_{i \in \calD} q_i$, $\calI = \set{0, \dots, \calQ - 1}$ and $\calI_i = \set{0, \dots, q_i - 1}$ be index sets, and $x$ and $x_\calD$ be indeterminates.
- Then, we have the following isomorphism $\eta$ for
    \\[
    \frac{R[x]}{\ideal{x^\calQ - 1}} \cong \Otimes_{i \in \calD} \frac{R[x_i]}{\ideal{x_i^{q_i} - 1}}
    \\]
    by sending $x$ to $\prod_{i \in \calD} x_i$.
- $x \mapsto \prod_{i \in \calD} x_i$ corresponds to the following isomorphism of NTTs
    \\[
    \left( \ba(x) \mapsto \ba(\omega_\calQ^\calI) \right) \cong \Otimes_{i \in \calD} \left( \ba_i(x_i) \mapsto \ba_i(\omega_{q_i}^{\calI_i}) \right)
    \\]
    where $\omega_{q_i} = \omega_\calQ^{e_i}$ and $e_\calI$ is the system of idempotents realizing $n \equiv \sum_{i \in \calD} e_i (n \bmod q_i) \pmod{\calQ}$.
- $x^l \mapsto \prod_{i \in \calD} x_i$ for an $l$ coprime to $\calQ$ is also a choice of multi-dimensional transform.
    - Ruritanian: choose $l = \left( \sum_{i \in \calD} \frac{\calQ}{q_i} \right)^{-1} \bmod \calQ$.
- As an isomorphism from a group algebra to a tensor product of associative algebras.

## "A" Multi-Dimensional Transform

We begin with multiplying two polynomials $\ba(x) = \sum_{i = 0}^5 a_i x^i$ and $\bb(x) = \sum_{i = 0}^5 b_i x^i$ in
the polynomial ring $\frac{R[x]}{\ideal{x^6 - 1}}$.
It is clear that the result $\bc(x) = \sum_{i = 0}^5 c_i x^i$ is
\\[
\\begin{pmatrix}
c_0 & 1 \\newline
c_1 & 1 \\newline
c_2 & 1 \\newline
\\end{pmatrix}
\\]

### Examples

## Convolutions

### Counting the Number of Convolutions

### Counting the Number of Multi-Dimensional Transforms

### Automorphisms on the additive group $(\mZ_\calQ, +, 0)$

## As Associative Algebra Isomorphisms

### Contents

