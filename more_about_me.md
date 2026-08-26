# More about me

[Back to the main page](./index.html).

## High-performance implementation

My core is the arithmetic of lattice-based schemes -- the polynomial multiplications behind NTRU, NTRU Prime, Saber, and the NIST standards ML-KEM and ML-DSA -- optimized across a wide range of platforms, from Cortex-M microcontrollers to Armv8-A Neon and AVX2 vector units.

I wrote the field's survey of polynomial multiplication for lattice-based cryptography (CiC 2024, single-authored). On microcontrollers, my coauthors and I set speed records for NTRU, NTRU Prime, Saber, Kyber, and Dilithium with Good--Thomas, multi-moduli NTTs, and the Fermat number transform. On vector units, my coauthors and I built multipliers for NTRU and NTRU Prime on Armv8-A Neon and optimized NTRU and Saber on AVX2; my own truncated-Rader NTRU Prime multiplier outperforms Daniel J. Bernstein's AVX2 code by 1.99x on Haswell and 2.16x on Skylake (ACISP 2024, single-authored). [Read more](./high_performance.html).

## Protocol level (USENIX Security 2026)

I also work above the arithmetic: *Shadowfax* shows how deniability can be preserved in post-quantum and hybrid authenticated key exchange, instantiated with ML-KEM and Falcon; I was responsible for the portable implementations.

## Formal verification

Besides optimizing assembly, I prove it correct, mainly with CryptoLine. My coauthors and I verified the assembly-optimized NTT multiplications of Kyber, Saber, and NTRU on Cortex-M4 and AVX2, the first verification of NTT multiplications in assembly (TCHES 2022(4)). I modeled Falcon's emulated floating-point arithmetic in CryptoLine, found that the multiplication in the submission package does not honor its claimed behavior, and showed that the discrepancy does not affect Falcon (IWSEC 2024, single-authored). As a contributing author on the EasyCrypt work behind the first formally verified ML-KEM whose performance is comparable to the fastest unverified AVX2 code, I proposed the optimizations of the compression functions and wrote that part of the paper (IEEE S&P 2025). [Read more](./formal_verification.html).

## Current directions

I'm currently accelerating the elliptic-curve discrete logarithm on H100 GPUs and extending my
low-level work to Armv9-A and AVX-512.
