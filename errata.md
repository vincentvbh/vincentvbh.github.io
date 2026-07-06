
# Errata — Software Implementations of Polynomial Multiplications for Lattice-Based Cryptosystems

Errata for the printed dissertation (`dissertation_printed.pdf`,
ISBN 9789465152516, DOI 10.54195/9789465152516). All items below
are in Chapter 8 "Platforms". In every case the prose adjacent
to the table states the correct semantics; the defects are
confined to the table cells. Page numbers refer to the printed
pagination.

## Table defects

- **Table 8.1 (p. 91), Armv7-M memory operations.** The load
  row's Signed/Unsigned columns are swapped: `ldrb`/`ldrh`
  (zero-extending, i.e. unsigned) appear under "Signed" and
  `ldrsb`/`ldrsh` (sign-extending, i.e. signed) under
  "Unsigned". The prose on p. 90 defines them correctly.
- **Table 8.10 (p. 101), Armv8-A Neon transfers.** The first
  `dup` row pairs a scalar destination `B`/`H`/`S`/`D` with a
  `w`/`x` source; no scalar-dup-from-general-register encoding
  exists. DUP (general) writes a vector arrangement, so the
  destination should read "Vector".
- **Table 8.13 (p. 103), additions and subtractions.** The
  scalar `add`/`sub` and `neg` rows claim `B`/`H`/`S`/`D`; the
  non-saturating scalar forms exist only as `D`. (The
  saturating `sqneg`, `{u, s}qadd`, `{u, s}qsub` entries are
  correct.)
- **Table 8.14 (p. 104), widening and narrowing.** Both widen
  rows have a wrong Source column: `{u, s}xtl` prints
  `8H`/`4S`/`2D` where it should be `8B`/`4H`/`2S`, and
  `{u, s}xtl2` prints `16H`/`8S`/`4D` — arrangements that do
  not exist — where it should be `16B`/`8H`/`4S`.
- **Table 8.15 (p. 104), comparisons.** The scalar rows claim
  `B`/`H`/`S`/`D`; scalar `cmeq`, `cm{ge, gt, hs, hi}`, and
  `cm{le, lt}` exist only as `D`.
- **Table 8.16 (p. 105), bitwise operations.** The `bic`
  immediate row prints `8B`/`16B`; BIC (vector, immediate)
  exists only for the `4H`/`8H`/`2S`/`4S` arrangements (the
  8-bit-element immediate operations are MOVI/MVNI).
- **Table 8.26 (p. 113), AVX2 multiplications.** The
  `vpmul{d, ud}q` row has Destination and Source swapped: it
  prints 8 x 32 <- 4 x 64, but the instruction computes 64-bit
  products of 32-bit elements, i.e. 4 x 64 <- 8 x 32.
- **Table 8.27 (p. 114), Cortex-M3 timings.** `revh` is not an
  Armv7-M mnemonic; it should be `revsh` (the p. 91 prose uses
  `revsh` correctly).

## Minor imprecisions

- **Table 8.19 (p. 106).** The `{, r}shrn{, 2}` rows give the
  immediate as `imm4`, which caps at 16; the `2S` <- `2D`
  narrowing shift admits shifts up to 32.
- **Table 8.20 (p. 107).** The `{u, s}qshl` and `sqshlu`
  immediate scalar rows list only `D`, though the saturating
  scalar forms exist for `B`/`H`/`S`/`D`; the `{u, s}shll{, 2}`
  rows omit the immediate operand from the Source column.
- **Table 8.25 (p. 112), AVX2 shifts.** `vpsravd` gets only the
  4 x 32 row; the 8 x 32 form is missing, while
  `vps{l, r}lvd` list both.

## Section 8.2.3.2 throughput labeling

In Section 8.2.3.2 (Cortex-A72, pp. 115-117), the figures
labeled "inverse throughput" are per-cycle throughputs from the
Cortex-A72 Software Optimization Guide: every printed 2 is a
true inverse throughput of 0.5 (`dup` lane, `mov` element,
permutations, `xtn`, additions and subtractions, comparisons,
bitwise operations), and every printed 0.5 is a true inverse
throughput of 2 (`str`, `sri`, shifts by register, and
non-widening multiplications, each with a 128-bit source
register). Figures of 1 are unaffected. The `sli` sentence
("1 with a 64-bit source register and 2 with a 128-bit source
register") already states the true inverse throughput. Section
8.2.4 (Firestorm) uses inverse throughput consistently with the
definition in Section 8.2.
