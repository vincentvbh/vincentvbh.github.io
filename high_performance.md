# High-performance implementation

[Back to More about me](./more_about_me.html).

A paper that spans several subsections is listed under each: TCHES 2021(2) covers NTRU and Saber on both Cortex-M4 and AVX2, and ACISP 2024 covers NTRU Prime on both Neon and AVX2.

## The toolbox and the survey (CiC 2024, single-authored)

My implementations draw on a full FFT/NTT toolbox -- Good--Thomas (and its incomplete/truncated variants), Rader and truncated Rader, Schönhage, Nussbaumer, Bruun's FFT, Toeplitz matrix-vector products, and the Fermat number transform -- together with the Barrett/Montgomery multiplication. I wrote the field's survey of polynomial multiplication for lattice-based cryptography, which organizes these techniques for rings of the form Z_q[x]/(x^n - αx - β) around modular arithmetic, homomorphisms, and vectorization.

## Microcontrollers

On microcontrollers my coauthors and I set speed records for NTRU, NTRU Prime, Saber, Kyber, and Dilithium with NTT-based multiplications -- Good--Thomas, multi-moduli NTTs, and the Fermat number transform for Dilithium.

### NTRU and NTRU Prime on Cortex-M4 (TCHES 2021(1), 2021(2), 2022(4))

We proposed NTT-based polynomial multiplications for NTRU Prime built on the Good--Thomas FFT and migrated the approach to all parameter sets of NTRU; I was deeply involved in the Good--Thomas implementation and in the Cortex-M4 implementations. We then revisited both schemes with NTTs that each support several parameters of NTRU and NTRU Prime, improving the initial and odd-radix butterflies of the Good--Thomas FFT and adding incomplete Good--Thomas variants for code size; I was the main contributor to this line.

### Saber on Cortex-M3 and Cortex-M4 (TCHES 2021(2), 2022(1))

After optimizing Saber on Cortex-M4 with NTTs over NTT-unfriendly rings, we moved to multi-moduli NTTs: we optimized Saber on Cortex-M3, the memory footprint on both cores, and the masked implementation on Cortex-M4, and concluded that the NTT is the fastest approach for Saber. I was the main contributor to the multi-moduli NTTs, which set the speed and stack records on Cortex-M3 and Cortex-M4 (including a masked Saber on Cortex-M4).

### Kyber and Dilithium on Cortex-M4 (ACNS 2022)

We revisited Kyber and Dilithium on Cortex-M4, incorporating assembly optimizations from prior Cortex-M4 and Cortex-A72 work (idea-wise) and optimizing the challenge polynomial multiplication in Dilithium; I proposed the Fermat number transform for that multiplication and an optimization of the base multiplication in Kyber.

### Without powerful multiplication instructions (TCHES 2025(1))

On targets *without* powerful multiplication instructions -- Cortex-M3 and 8-bit AVR -- I was again the main contributor and implemented the Cortex-M3 side: we generalized Barrett multiplication to multi-limb arithmetic for Dilithium's prime modulus and showed that Nussbaumer's transform wins for Saber's power-of-two modulus.

### Big-integer multiplication (IWSEC 2022)

On Cortex-M3/M55 we located the crossover between FFT-based and quadratic integer multiplication at around 2048 bits; I was involved in the Cortex-M3 implementation.

## Vector units

### Armv8-A Neon (TCHES 2022(1), INDOCRYPT 2023, ACNS 2024; ACISP 2024, single-authored)

With Armv8-A Neon on Cortex-A72 and Apple M1, we worked out the multiplicative form of Barrett reduction and its correspondence with Montgomery multiplication -- a rediscovery, as we learned after publication -- and I implemented it for Dilithium, Kyber, and Saber.

For NTRU and NTRU Prime we built vectorized multipliers from Toom--Cook, Toeplitz matrix-vector products, and Schönhage's, Bruun's, Good--Thomas, and Rader's FFTs, with me as the main contributor for NTRU Prime. For NTRU, I proposed the Toom--Cook improvement and integrated and further optimized the coauthors' multipliers; for NTRU Prime, I proposed the optimizations, implemented Bruun's FFT and the fastest approach, and wrote the paper.

### AVX2 (TCHES 2021(2); ACISP 2024, single-authored)

With AVX2 we optimized NTRU and Saber over NTT-unfriendly rings on Skylake. For NTRU Prime, my truncated-Rader-based implementation outperforms Daniel J. Bernstein's state-of-the-art AVX2 code (OpenSSLNTRU, USENIX Security 2022) by 1.99x on Haswell and 2.16x on Skylake.
