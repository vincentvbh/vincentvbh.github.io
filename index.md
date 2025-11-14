

Hi, there. I'm Vincent Hwang (黃柏文).
I'm currently a PhD student supervised by [Peter Schwabe](https://cryptojedi.org/peter/index.shtml) (樂岩) at Max Planck Institute for Security and Privacy.
Before joining the PhD program in January 2023, I obtained my master's degree under the supervision of [Yen-Huan Li](https://sites.google.com/site/yenhuanli/home) (李彥寰) in June 2022.
I mostly worked with [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html) (楊柏因).
In particular, I was (and am) focusing on implementing number-theoretic transforms used in the lattice-based cryptosystems Dilithium, Kyber, NTRU, NTRU Prime, and Saber.
My master thesis focuses on the following platforms:
- Cortex-M3:
    - Saber
- Cortex-M4:
    - NTRU
    - NTRU Prime
    - Saber
- Cortex-A72:
    - Dilithium
    - Kyber
    - Saber

You can find the details of the master thesis [here](https://github.com/vincentvbh/NTTs_with_Armv7-M_Armv7E-M_Armv8-A).

While I was an undergraduate student (Sept. 2016 -- Jun. 2021), I spent most of the time on Theoretical Computer Science, in particular, graph algorithms and generalizations of sorting problems.

# Curriculum Vitae
- [CV](https://vincentvbh.github.io/CV.pdf) (version 2025-10-31)

# Contact
- Email: vincentvbh7 at gmail dot com

# Research Interests
- Assembly programming with Armv7-M, Armv7E-M, Armv8-A, AVX2
- Practical integer and polynomial multiplications
- Post-quantum cryptography (mainly lattice-based)
- Formal verification (still exploring)
- GPU programming (ongoing research)

# Programming Skills
- Assembly (Armv7E-M, Armv8-A, AVX2, very familiar)
- Assembly (Armv9-A, AVX-512, somewhat familiar)
- C (very familiar)
- C++ (somewhat familiar), CUDA (somewhat familiar)
- Haskell (some experience)

# Services
- 2026:
    -  Reviewer of [TCHES 2026](https://ches.iacr.org/2026) (x1), (Incoming) Artifact Evaluation Committee Member of [TCHES 2026](https://ches.iacr.org/2026/)
- 2025:
    - Reviewer of [TCHES 2025](https://ches.iacr.org/2025/) (x8), [ArcticCrypt 2025](https://simula-uib.com/arcticcrypt2025/) (x1), [CT-RSA 2025](https://ct-rsa-2025.csa.iisc.ac.in/) (x2), [Journal of Cryptographic Engineering](https://link.springer.com/journal/13389) (x1)
    - Artifact Evaluation Committee Member of [TCHES 2025](https://ches.iacr.org/2025/) (x5)
- 2024:
    - Reviewer of [Crypto 2024](https://crypto.iacr.org/2024/) (x1), [TCHES 2024](https://ches.iacr.org/2024/) (x3)
- 2023:
    - Artifact Review Committee Member of [TCHES 2023](https://ches.iacr.org/2023/) (x2)

# Publications
- [Google Scholar](https://scholar.google.com.ec/citations?user=idEjFxoAAAAJ&hl=en)
- [DBLP](https://dblp.org/pid/277/3814.html)
- 2025:
    - Proving Faster Implementations Faster: Combining Deductive and Circuit-Based Reasoning in EasyCrypt
        - [José Bacelar Almeida](https://www.inesctec.pt/en/people/jose-bacelar-almeida), [Manuel Barbosa](https://www.dcc.fc.up.pt/~mbb/), [Gilles Barthe](https://gbarthe.github.io/), Gustavo Xavier Delerue Marinho Alves, [Luís Esquível](https://www.inesctec.pt/en/people/luis-esquivel-costa), **Vincent Hwang**, Tiago Oliveira, [Hugo Pacheco](https://www.dcc.fc.up.pt/~hpacheco/), [Peter Schwabe](https://cryptojedi.org/peter/index.shtml), [Pierre-Yves Strub](https://www.strub.nu/)
        - [IEEE Security and Privacy 2025, Cycle 2](https://sp2025.ieee-security.org/index.html)
        - [paper](https://www.computer.org/csdl/proceedings-article/sp/2025/223600d526/26hiVyFN8o8) [ePrint](https://eprint.iacr.org/2025/1607)
    - Multiplying Polynomials without Powerful Multiplication Instructions (Long Paper)
        - **Vincent Hwang**, [YoungBeom Kim](https://whybe.notion.site/YoungBeom-Kim-217f1235666e4e368565767c0bdc0926), and [Seog Chung Seo](https://sites.google.com/kookmin.ac.kr/cselab/members/professor)
        - [IACR Transactions on Cryptographic Hardware and Embedded Systems (TCHES 2025), Issue 1](https://ches.iacr.org/2025/)
        - [paper](https://vincentvbh.github.io/papers/TCHES2025_1_06.pdf) [slides](https://vincentvbh.github.io/slides/TCHES2025_1_21_slides.pdf) [code](https://github.com/vincentvbh/PolyMul_Without_PowerfulMul) [ePrint](https://eprint.iacr.org/2024/1649)
- 2024:
    - Formal Verification of Emulated Floating-Point Arithmetic in Falcon
        - **Vincent Hwang**
        - [International Workshop on Security (IWSEC 2024)](https://www.iwsec.org/2024/)
        - [paper](https://link.springer.com/chapter/10.1007/978-981-97-7737-2_7) [slides](https://vincentvbh.github.io/slides/IWSEC2024_1_slides.pdf) [code](https://github.com/vincentvbh/Float_formal) [ePrint](https://vincentvbh.github.io/papers/2024-321.pdf)
    - A Survey of Polynomial Multiplications for Lattice-Based Cryptosystems
        - **Vincent Hwang**
        - [Communications in Cryptology (CiC 2024), Issue 2](https://cic.iacr.org/)
        - [paper](https://vincentvbh.github.io/papers/CiC2024_2_1.pdf) [code](https://github.com/Polynomial-Multiplications-for-Lattices/Polynomial-Multiplications-for-Lattices) [ePrint](https://vincentvbh.github.io/papers/2023-1962.pdf)
    - Pushing the Limit of Vectorized Polynomial Multiplication for NTRU Prime
        - **Vincent Hwang**
        - [Australasian Conference for Security and Privacy (ACISP 2024)](https://www.acisp24.com/)
        - [paper](https://link.springer.com/chapter/10.1007/978-981-97-5028-3_5) [slides](https://vincentvbh.github.io/slides/ACISP2024_2_97_slides.pdf) [code](https://github.com/vector-polymul-ntru-ntrup/NTRU_Prime_truncation) [ePrint](https://vincentvbh.github.io/papers/2023-604.pdf)
    - Algorithmic Views of Vectorized Polynomial Multipliers -- NTRU Prime
        - **Vincent Hwang**, Chi-Ting Liu, and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html)
        - [Applied Cryptography and Network Security (ACNS 2024)](https://wp.nyu.edu/acns2024/)
        - [paper](https://vincentvbh.github.io/papers/ACNS2024_1_21.pdf) [slides](https://vincentvbh.github.io/slides/ACNS2024_1_21_slides.pdf) [code](https://github.com/vector-polymul-ntru-ntrup/NTRU_Prime) [ePrint](https://vincentvbh.github.io/papers/2023-1580.pdf)
- 2023:
    - Algorithmic Views of Vectorized Polynomial Multipliers -- NTRU
        - Han-Ting Chen, [Yi-Hua Chung](https://yi-huaaa.github.io/about/), **Vincent Hwang**, and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html)
        - [International Conference on Cryptology in India (INDOCRYPT 2023)](https://crsind.in/indocrypt2023/)
        - [paper](https://vincentvbh.github.io/papers/INDOCRYPT2023_28.pdf) [slides](https://vincentvbh.github.io/slides/IndoCrypt2023_slides.pdf) [code](https://github.com/vector-polymul-ntru-ntrup/NTRU) [ePrint](https://vincentvbh.github.io/papers/2023-1637.pdf)
- 2022:
    - Verified NTT Multiplications for NISTPQC KEM Lattice Finalists: Kyber, SABER, and NTRU
        - **Vincent Hwang**, Jiaxiang Liu, Gregor Seiler, Xiaomu Shi, Ming-Hsien Tsai, [Bow-Yaw Wang](https://homepage.iis.sinica.edu.tw/~bywang/), and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html)
        - [IACR Transactions on Cryptographic Hardware and Embedded Systems (TCHES 2022), Issue 4](https://ches.iacr.org/2022/)
        - [paper](https://vincentvbh.github.io/papers/TCHES2022_4_26.pdf) [talk by Bo-Yin Yang](https://youtu.be/TSUtA5hmrtk?t=4011) [slides](https://vincentvbh.github.io/slides/TCHES2022_4_26_slides.pdf) [code](https://github.com/fmlab-iis/cryptoline)
    - Multi-Parameter Support with NTTs for NTRU and NTRU Prime on Cortex-M4
        - [Erdem Alkim](https://erdemalkim.github.io/), **Vincent Hwang**, and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html)
        - [IACR Transactions on Cryptographic Hardware and Embedded Systems (TCHES 2022), Issue 4](https://ches.iacr.org/2022/)
        - [paper](https://vincentvbh.github.io/papers/TCHES2022_4_13.pdf) [talk by myself](https://youtu.be/TSUtA5hmrtk?t=2825) [slides](https://vincentvbh.github.io/slides/TCHES2022_4_13_slides.pdf) [code](https://github.com/vincentvbh/multi-params-ntt_NTRU_NTRUPrime) [ePrint](https://vincentvbh.github.io/papers/2022-930.pdf)
    - Efficient Multiplication of Somewhat Small Integers using Number-Theoretic Transforms (Best Paper Award)
        - Hanno Becker, **Vincent Hwang**, [Matthias J. Kannwischer](https://kannwischer.eu), [Lorenz Panny](https://yx7.cc/), and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html)
        - [International Workshop on Security (IWSEC 2022)](https://www.iwsec.org/2022/index.html)
        - [paper](https://link.springer.com/chapter/10.1007/978-3-031-15255-9_1) [slides](https://vincentvbh.github.io/slides/20220831_ntt-int-mul_slides.pdf) [code](https://github.com/ntt-int-mul/ntt-int-mul-m3) [ePrint](https://vincentvbh.github.io/papers/2022-439.pdf)
    - Faster Kyber and Dilithium on the Cortex-M4
        - [Amin Abdulrahman](https://abdulrahman.de/), **Vincent Hwang**, [Matthias J. Kannwischer](https://kannwischer.eu), and [Amber Sprenkels](https://electricdusk.com/)
        - [Applied Cryptography and Network Security (ACNS 2022)](https://acns22.di.uniroma1.it/)
        - [paper](https://vincentvbh.github.io/papers/ACNS2022_202.pdf) [code](https://github.com/FasterKyberDilithiumM4/FasterKyberDilithiumM4) [ePrint](https://vincentvbh.github.io/papers/2022-112.pdf)
    - Neon NTT: Faster Dilithium, Kyber, and Saber on Cortex-A72 and Apple M1
        - Hanno Becker, **Vincent Hwang**, [Matthias J. Kannwischer](https://kannwischer.eu), [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html), and Shang-Yi Yang
        - [IACR Transactions on Cryptographic Hardware and Embedded Systems (TCHES 2022)](https://ches.iacr.org/2022/)
        - [paper](https://vincentvbh.github.io/papers/TCHES2022_1_08.pdf) [talk by Hanno Becker](https://youtu.be/TSUtA5hmrtk?t=1491) [slides](https://vincentvbh.github.io/slides/TCHES2022_1_08_slide.pptx) [code](https://github.com/neon-ntt/neon-ntt) [ePrint](https://vincentvbh.github.io/papers/2021-986.pdf)
    - Multi-moduli NTTs for Saber on Cortex-M3 and Cortex-M4
        - [Amin Abdulrahman](https://abdulrahman.de/), Jiun-Peng Chen, Yu-Jia Chen, **Vincent Hwang**, [Matthias J. Kannwischer](https://kannwischer.eu), and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html)
        - [IACR Transactions on Cryptographic Hardware and Embedded Systems (TCHES 2022)](https://ches.iacr.org/2022/)
        - [paper](https://vincentvbh.github.io/papers/TCHES2022_1_05.pdf) [talk](https://youtu.be/TSUtA5hmrtk?t=179) [slides](https://vincentvbh.github.io/slides/TCHES2022_1_05_slides.pdf) [slide (updated)](https://vincentvbh.github.io/slides/TCHES2022_1_05_slides_updated.pdf) [code](https://github.com/multi-moduli-ntt-saber/multi-moduli-ntt-saber) [ePrint](https://vincentvbh.github.io/papers/2021-995.pdf)
- 2021:
    - NTT Multiplication for NTT-unfriendly Rings
        - Chi-Ming Marvin Chung, **Vincent Hwang**, [Matthias J. Kannwischer](https://kannwischer.eu), Gregor Seiler, Cheng-Jhih Shih, and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html)
        - [IACR Transactions on Cryptographic Hardware and Embedded Systems (TCHES 2021), Issue 2](https://ches.iacr.org/2021/)
        - [paper](https://vincentvbh.github.io/papers/TCHES2021_2_06.pdf) [talk](https://youtube.com/watch?v=a9_-jhD2ZG0) [slides](https://vincentvbh.github.io/slides/TCHES2021_2_06.slides.pdf) [code](https://github.com/ntt-polymul/ntt-polymul) [ePrint](https://vincentvbh.github.io/papers/2020-1397.pdf)
    - Polynomial Multiplication in NTRU Prime
        - [Erdem Alkim](https://erdemalkim.github.io/), Dean Yun-Li Cheng, Chi-Ming Marvin Chung, Hülya Evkan, Leo Wei-Lun Huang, **Vincent Hwang**, Ching-Lin Trista Li, [Ruben Niederhagen](http://polycephaly.org/), Cheng-Jhih Shih, Julian Wälde, and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html)
        - [IACR Transactions on Cryptographic Hardware and Embedded Systems (TCHES 2021), Issue 1](https://ches.iacr.org/2021/)
        - [paper](https://vincentvbh.github.io/papers/TCHES2021_1_09.pdf) [talk](https://youtube.com/watch?v=F95gXPfXrBA) [slides](https://vincentvbh.github.io/slides/TCHES2021_1_09_slides.pdf) [code](https://github.com/vincentvbh/NTRUPrime-PolyMul) [ePrint](https://vincentvbh.github.io/papers/2020-1216.pdf)

# Technical Reports
- [IACR ePrint](https://eprint.iacr.org/search?q=%22Vincent+Hwang%22)
- 2025:
    - Shadowfax: Combiners for Deniability
        - [Phillip Gajland](https://gaphil.github.io/), **Vincent Hwang**, [Jonas Janneck](https://jonasjanneck.org/)
        - IACR ePrint
        - [ePrint](https://eprint.iacr.org/2025/154) [code](https://github.com/vincentvbh/shadowfax)
- 2024:
- 2023:
    - Barrett Multiplication for Dilithium on Embedded Devices
        - **Vincent Hwang**, [YoungBeom Kim](https://whybe.notion.site/YoungBeom-Kim-217f1235666e4e368565767c0bdc0926), and [Seog Chung Seo](https://sites.google.com/kookmin.ac.kr/cselab/members/professor)
        - IACR ePrint
        - [ePrint](https://eprint.iacr.org/2023/1955) [code](https://github.com/vincentvbh/Barrett_Dilithium_Embedded)
        - This paper was extended into the follow paper:
            - Multiplying Polynomials without Powerful Multiplication Instructions (Long Paper)
    - Algorithmic Views of Vectorized Polynomial Multipliers for NTRU and NTRU Prime (Long Paper)
        - Han-Ting Chen, [Yi-Hua Chung](https://yi-huaaa.github.io/about/), **Vincent Hwang**, Chi-Ting Liu, and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html)
        - IACR ePrint
        - [ePrint](https://eprint.iacr.org/2023/541)
        - This paper was split into the following papers:
            - Algorithmic Views of Vectorized Polynomial Multipliers -- NTRU
            - Algorithmic Views of Vectorized Polynomial Multipliers -- NTRU Prime


