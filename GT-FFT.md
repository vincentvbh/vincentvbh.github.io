
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
c_0 \\newline
c_1 \\newline
c_2 \\newline
c_3 \\newline
c_4 \\newline
c_5
\\end{pmatrix}
=
\\begin{pmatrix}
a_0 b_0 + a_1 b_5 + a_2 b_4 + a_3 b_3 + a_4 b_2 + a_5 b_1 \\newline
a_0 b_1 + a_1 b_0 + a_2 b_5 + a_3 b_4 + a_4 b_3 + a_5 b_2 \\newline
a_0 b_2 + a_1 b_1 + a_2 b_0 + a_3 b_5 + a_4 b_4 + a_5 b_3 \\newline
a_0 b_3 + a_1 b_2 + a_2 b_1 + a_3 b_0 + a_4 b_5 + a_5 b_4 \\newline
a_0 b_4 + a_1 b_3 + a_2 b_2 + a_3 b_1 + a_4 b_0 + a_5 b_5 \\newline
a_0 b_5 + a_1 b_4 + a_2 b_3 + a_3 b_2 + a_4 b_1 + a_5 b_0
\\end{pmatrix},
\\]
requiring $36$ multiplications and $30$ additions.

We propose the following computations with only $24$ multiplications and $30$ additions/subtractions.
We first compute
\\[
\\begin{pmatrix}
a_0' \\newline
a_1' \\newline
a_2' \\newline
a_3' \\newline
a_4' \\newline
a_5' \\newline
\\end{pmatrix}
=
\\begin{pmatrix}
a_0 + a_3 \\newline
-a_1 + a_4 \\newline
a_2 + a_5 \\newline
a_0 - a_3 \\newline
a_1 + a_4 \\newline
a_2 - a_5 \\newline
\\end{pmatrix}
\\]
and
\\[
\\begin{pmatrix}
b_0' \\newline
b_1' \\newline
b_2' \\newline
b_3' \\newline
b_4' \\newline
b_5' \\newline
\\end{pmatrix}
=
\\begin{pmatrix}
b_0 + b_3 \\newline
-b_1 + b_4 \\newline
b_2 + b_5 \\newline
b_0 - b_3 \\newline
b_1 + b_4 \\newline
b_2 - b_5 \\newline
\\end{pmatrix}.
\\]
Then, we convolute $(a_0', a_1', a_2')$ with $(b_0', b_1', b_2')$ and $(a_3', a_4', a_5')$ with $(b_3', b_4', b_5')$.
Now we have
\\[
\\begin{pmatrix}
c_0' \\newline
c_1' \\newline
c_2' \\newline
\\end{pmatrix}
=
\\begin{pmatrix}
a_0' b_0' + a_1' b_2' + a_2' b_1' \\newline
a_0' b_1' + a_1' b_0' + a_2' b_2' \\newline
a_0' b_2' + a_1' b_1' + a_2' b_0' \\newline
\\end{pmatrix}
\\]
and
\\[
\\begin{pmatrix}
c_4' \\newline
c_5' \\newline
c_6' \\newline
\\end{pmatrix}
=
\\begin{pmatrix}
a_4' b_4' + a_5' b_6' + a_6' b_5' \\newline
a_4' b_5' + a_5' b_4' + a_6' b_6' \\newline
a_4' b_6' + a_5' b_5' + a_6' b_4' \\newline
\\end{pmatrix}.
\\]

### Examples

## Convolutions

### Counting the Number of Convolutions

### Counting the Number of Multi-Dimensional Transforms

### Automorphisms on the additive group $(\mZ_\calQ, +, 0)$

## As Associative Algebra Isomorphisms

### Contents

