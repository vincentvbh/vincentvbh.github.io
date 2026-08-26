# More about me

[Back to the main page](./index.html).

## High-performance implementation

My core is the arithmetic of lattice-based schemes -- the polynomial multiplications behind NTRU, NTRU Prime, Saber, and the NIST standards ML-KEM and ML-DSA -- optimized across a wide range of platforms, from Cortex-M microcontrollers to Armv8-A Neon and AVX2 vector units.

### The toolbox and the survey

My implementations draw on a full FFT/NTT toolbox -- Good--Thomas (and its incomplete/truncated variants), Rader and truncated Rader, Schönhage, Nussbaumer, Bruun's FFT, Toeplitz matrix-vector products, and the Fermat number transform -- together with the Barrett/Montgomery multiplication. I wrote the field's survey of polynomial multiplication for lattice-based cryptography (sole-authored, CiC 2024), which organizes these techniques for rings of the form Z_q[x]/(x^n - αx - β) around modular arithmetic, homomorphisms, and vectorization.

### Microcontrollers

On microcontrollers my coauthors and I set speed records for NTRU, NTRU Prime, Saber, Kyber, and Dilithium with NTT-based multiplications -- Good--Thomas, multi-moduli NTTs, and the Fermat number transform for Dilithium.

#### NTRU and NTRU Prime on Cortex-M4

We proposed NTT-based polynomial multiplications for NTRU Prime built on the Good--Thomas FFT and migrated the approach to all parameter sets of NTRU; I was deeply involved in the Good--Thomas implementation and in the Cortex-M4 implementations. We then revisited both schemes with NTTs that each support several parameters of NTRU and NTRU Prime, improving the initial and odd-radix butterflies of the Good--Thomas FFT and adding incomplete Good--Thomas variants for code size; I was the main contributor to this line.

#### Saber on Cortex-M3 and Cortex-M4

After optimizing Saber on Cortex-M4 with NTTs over NTT-unfriendly rings, we moved to multi-moduli NTTs: we optimized Saber on Cortex-M3, the memory footprint on both cores, and the masked implementation on Cortex-M4, and concluded that the NTT is the fastest approach for Saber. I was the main contributor to the multi-moduli NTTs, which set the speed and stack records on Cortex-M3 and Cortex-M4 (including a masked Saber on Cortex-M4).

#### Kyber and Dilithium on Cortex-M4

We revisited Kyber and Dilithium on Cortex-M4, incorporating assembly optimizations from prior Cortex-M4 and Cortex-A72 work (idea-wise) and optimizing the challenge polynomial multiplication in Dilithium; I proposed the Fermat number transform for that multiplication and an optimization of the base multiplication in Kyber.

#### Without powerful multiplication instructions

On targets *without* powerful multiplication instructions -- Cortex-M3 and 8-bit AVR -- I was again the main contributor and implemented the Cortex-M3 side: we generalized Barrett multiplication to multi-limb arithmetic for Dilithium's prime modulus and showed that Nussbaumer's transform wins for Saber's power-of-two modulus.

#### Big-integer multiplication

On Cortex-M3/M55 we located the crossover between FFT-based and quadratic integer multiplication at around 2048 bits; I was involved in the Cortex-M3 implementation.

### Vector units

#### Armv8-A Neon

With Armv8-A Neon on Cortex-A72 and Apple M1, we worked out the multiplicative form of Barrett reduction and its correspondence with Montgomery multiplication -- a rediscovery, as we learned after publication -- and I implemented it for Dilithium, Kyber, and Saber.

For NTRU and NTRU Prime we built vectorized multipliers from Toom--Cook, Toeplitz matrix-vector products, and Schönhage's, Bruun's, Good--Thomas, and Rader's FFTs, with me as the main contributor for NTRU Prime. For NTRU, I proposed the Toom--Cook improvement and integrated and further optimized the coauthors' multipliers; for NTRU Prime, I proposed the optimizations, implemented Bruun's FFT and the fastest approach, and wrote the paper.

#### AVX2

With AVX2 we optimized NTRU and Saber over NTT-unfriendly rings on Skylake. For NTRU Prime, my truncated-Rader-based implementation outperforms Daniel J. Bernstein's state-of-the-art AVX2 code (OpenSSLNTRU, USENIX Security 2022) by 1.99x on Haswell and 2.16x on Skylake.

## Protocol level

I also work above the arithmetic: *Shadowfax* (USENIX Security 2026) shows how deniability can be preserved in post-quantum and hybrid authenticated key exchange, instantiated with ML-KEM and Falcon; I was responsible for the portable implementations.

## Formal verification

Besides optimizing assembly, I prove it correct. My main tool is CryptoLine, a domain-specific language for arithmetic assembly whose backends pair a computer algebra system (for the algebraic identities) with an SMT solver (for the bit-level range and overflow checks); I have also worked with Jasmin and EasyCrypt.

### Verified NTT multiplications for Kyber, Saber, and NTRU (TCHES 2022)

We verified the assembly-optimized NTT-based polynomial multiplications of Kyber, Saber, and NTRU on Cortex-M4 and on Skylake with AVX2 -- six instances, and the first verification of NTT multiplications in assembly. For each instance CryptoLine checks the algebraic correctness of the transforms, the absence of overflows, and the coefficient ranges; to make the six instances tractable we extended CryptoLine with non-local compositional reasoning (cuts), without which the verification is much slower or impossible. I rewrote the Cortex-M4 assembly polynomial multiplication for NTRU and described the structure of the Cortex-M4 assembly programs in the paper.

### Emulated floating-point arithmetic in Falcon (IWSEC 2024, sole-authored)

Falcon's signature generation runs its complex FFT on constant-time, software-emulated floating-point arithmetic. I modeled the emulated addition, subtraction, and multiplication in CryptoLine and found that the multiplication in the submission package does not honor its claimed behavior: because the zeroization of too-small results precedes the rounding increment, some products whose absolute value is the smallest positive normal double are zeroized, and 692 of the 2048 floating-point constants in the FFT admit operands that trigger it. I then showed that the discrepancy does not affect Falcon: with a range arithmetic of my own that derives lower bounds -- not only the upper bounds usual in floating-point error analysis -- and with CryptoLine checking every pre- and post-condition, every non-zero intermediate value of the signature-generation FFT stays at least 2<sup>-529</sup> in absolute value, far from the threshold. Finally, I implemented my own emulated multiplication in Armv7-M assembly and in Jasmin and proved the assembly and Jasmin implementations of both addition and multiplication equivalent to the model, and hence to each other: the verification of highly optimized assembly transfers to the more readable Jasmin code.

### Hybrid deductive and circuit-based reasoning in EasyCrypt (IEEE S&P 2025)

I was a contributing author on the EasyCrypt work that combines deductive and circuit-based reasoning: selected fragments of a Jasmin program are turned into circuits and discharged by SAT-based equivalence checking while the surrounding proof stays deductive, which lets a proof for one implementation carry over to other implementations of the same computation. The result is the first formally verified ML-KEM whose performance is comparable to the fastest unverified AVX2 code, the verification of the AVX2 rejection sampling that prior work had left open, and a simpler verification of the vectorized Keccak permutation. My part was the compression functions: I proposed the optimizations -- a signed, rounding variant of Barrett reduction that drops the conditional subtraction, its precision pinned down by exhaustive testing where the analytical bound falls short -- and wrote the corresponding part of the paper. With circuit-based reasoning the proof of the new AVX2 routine took 100 lines instead of 650, and two Armv7-M compression routines, one on UMULL and one on the DSP instruction SMMULR, were proven extensionally equivalent to the x86-64 reference.

## Current directions

I'm currently accelerating the elliptic-curve discrete logarithm on H100 GPUs and extending my
low-level work to Armv9-A and AVX-512.
