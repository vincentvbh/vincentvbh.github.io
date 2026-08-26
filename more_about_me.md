# More about me

[Back to the main page](./index.html).

## High-performance implementation

My core is the arithmetic of lattice-based schemes -- the polynomial multiplications behind NTRU, NTRU Prime, Saber, and the NIST standards ML-KEM and ML-DSA -- optimized across a wide range of platforms, from Cortex-M microcontrollers to Armv8-A Neon and AVX2 vector units.

**Microcontrollers.** On Cortex-M4 my coauthors and I set speed records for NTRU, NTRU Prime, Saber, Kyber, and Dilithium with NTT-based multiplications -- Good--Thomas and its incomplete variants (also for code size), multi-moduli NTTs (including a masked Saber on Cortex-M3/M4), and the Fermat number transform for Kyber. On targets *without* powerful multiplication instructions -- Cortex-M3 and 8-bit AVR -- I generalized Barrett multiplication to multi-limb arithmetic for Dilithium's prime modulus and showed that Nussbaumer's transform wins for Saber's power-of-two modulus; on Cortex-M3/M55 we located the crossover between FFT-based and quadratic integer multiplication at around 2048 bits.

**Vector units.** With Armv8-A Neon on Cortex-A72 and Apple M1, we rediscovered the multiplicative form of Barrett reduction and its correspondence with Montgomery multiplication, and I implemented it for Dilithium, Kyber, and Saber; for NTRU and NTRU Prime we built vectorized multipliers from Toom--Cook, Toeplitz matrix-vector products, and Schönhage's, Bruun's, Good--Thomas, and Rader's FFTs. With AVX2 on Haswell/Skylake we optimized NTRU and Saber over NTT-unfriendly rings and NTRU Prime with truncated Rader's FFT.

**The toolbox and the survey.** My implementations draw on a full FFT/NTT toolbox -- Good--Thomas (and its incomplete/truncated variants), Rader and truncated Rader, Schönhage, Nussbaumer, Bruun's FFT, Toeplitz matrix-vector products, and the Fermat number transform -- together with the Barrett/Montgomery multiplication. I wrote the field's survey of polynomial multiplication for lattice-based cryptography (sole-authored, CiC 2024), which organizes these techniques for rings of the form Z_q[x]/(x^n - αx - β) around modular arithmetic, homomorphisms, and vectorization.

**Protocol level.** I also work above the arithmetic: *Shadowfax* (USENIX Security 2026) shows how deniability can be preserved in post-quantum and hybrid authenticated key exchange, instantiated with ML-KEM and Falcon; I was responsible for the portable implementations.

## Formal verification

I've also contributed to formal-verification efforts for optimized assembly cryptographic programs,
for example, the emulated floating-point arithmetic in Falcon (sole-authored, IWSEC 2024).

## Current directions

I'm currently accelerating the elliptic-curve discrete logarithm on H100 GPUs and extending my
low-level work to Armv9-A and AVX-512.
