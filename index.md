

Hi, there. I'm Vincent Hwang.
I'm currently a PhD student supervised by [Peter Schwabe](https://cryptojedi.org/peter/index.shtml)(樂岩) at Max Planck Institute for Security and Privacy.
Currently, I'm learning how to verify assembly-optimized implementations of post-quantum cryptosystems.
Before joining the PhD program, I obtained my master's degree under the supervision of [Yen-Huan Li](https://sites.google.com/site/yenhuanli/home) (李彥寰).
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

You can find the details [here](https://github.com/vincentvbh/NTTs_with_Armv7-M_Armv7E-M_Armv8-A).

I started studying assembly implementations of lattice-based cryptosystems when [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html) taught the course Post-Quantum Cryptography at National Taiwan University during the last two years of my undergraduate study.
While I was an undergraduate, I spent most of the time on Theoretical Computer Science, in particular, graph algorithms and generalizations of sorting problems.

# Contact
- Email: vincentvbh7@gmail.com.

# Research Interests
- Implementing number-theoretic transforms with Armv7-M, Armv7E-M, and Armv8-A.
- Algorithmic partial order problems.
- Graph algorithms.

# Committee Member
- Artifact Review Committee of [CHES 2023](https://ches.iacr.org/2023/)

# Publications
- [Google Scholar](https://scholar.google.com.ec/citations?user=idEjFxoAAAAJ&hl=en)
- Verified NTT Multiplications for NISTPQC KEM Lattice Finalists: Kyber, SABER, and NTRU.
    - **Vincent Hwang**, Jiaxiang Liu, Gregor Seiler, Xiaomu Shi, Ming-Hsien Tsai, Bow-Yaw Wang, and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html).
    - TCHES 2022 [paper](https://vincentvbh.github.io/papers/TCHES2022_4_26.pdf) [talk by Bo-Yin Yang](https://youtu.be/TSUtA5hmrtk?t=4011) [slide](https://vincentvbh.github.io/slides/TCHES2022_4_26_slide.pdf) [code](https://github.com/fmlab-iis/cryptoline)
- Multi-Parameter Support with NTTs for NTRU and NTRU Prime on Cortex-M4.
    - Erdem Alkim, **Vincent Hwang**, and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html).
    - TCHES 2022 [paper](https://vincentvbh.github.io/papers/TCHES2022_4_13.pdf) [talk by myself](https://youtu.be/TSUtA5hmrtk?t=2825) [slide](https://vincentvbh.github.io/slides/TCHES2022_4_13_slide.pdf) [code](https://github.com/vincentvbh/multi-params-ntt_NTRU_NTRUPrime) [ePrint](https://vincentvbh.github.io/papers/2022-930.pdf)
- Efficient Multiplication of Somewhat Small Integers using Number-Theoretic Transforms (Best Paper Award).
    - Hanno Becker, **Vincent Hwang**, [Matthias J. Kannwischer](https://kannwischer.eu), Lorenz Panny, and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html).
    - IWSEC 2022 [paper](https://vincentvbh.github.io/papers/978-3-031-15255-9_1.pdf) [slide](https://vincentvbh.github.io/slides/20220831_ntt-int-mul.pdf) [code](https://github.com/ntt-int-mul/ntt-int-mul-m3) [ePrint](https://vincentvbh.github.io/papers/2022-439.pdf).
- Faster Kyber and Dilithium on the Cortex-M4.
    - Amin Abdulrahman, **Vincent Hwang**, [Matthias J. Kannwischer](https://kannwischer.eu), and Daan Sprenkels.
    - ACNS 2022 [paper](https://vincentvbh.github.io/papers/978-3-031-15255-9_1.pdf) [code](https://github.com/FasterKyberDilithiumM4/FasterKyberDilithiumM4) [ePrint](https://vincentvbh.github.io/papers/2022-112.pdf).
- Multi-moduli NTTs for Saber on Cortex-M3 and Cortex-M4.
    - Amin Abdulrahman, Jiun-Peng Chen, Yu-Jia Chen, **Vincent Hwang**, [Matthias J. Kannwischer](https://kannwischer.eu), and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html).
    - TCHES 2022 [paper](https://vincentvbh.github.io/papers/TCHES2022_1_05.pdf) [talk by myself](https://youtu.be/TSUtA5hmrtk?t=179) [slide](https://vincentvbh.github.io/slides/TCHES2022_1_05_slide.pdf) [slide (updated)](https://vincentvbh.github.io/slides/TCHES2022_1_05_slide_updated.pdf) [code](https://github.com/multi-moduli-ntt-saber/multi-moduli-ntt-saber) [ePrint](https://vincentvbh.github.io/papers/2021-995.pdf).
- Neon NTT: Faster Dilithium, Kyber, and Saber on Cortex-A72 and Apple M1.
    - Hanno Becker, **Vincent Hwang**, [Matthias J. Kannwischer](https://kannwischer.eu), [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html), and Shang-Yi Yang.
    - TCHES 2022 [paper](https://vincentvbh.github.io/papers/TCHES2022_1_08.pdf) [talk by Hanno Becker](https://youtu.be/TSUtA5hmrtk?t=1491) [slide](https://vincentvbh.github.io/slides/TCHES2022_1_08_slide.pptx) [code](https://github.com/neon-ntt/neon-ntt) [ePrint](https://vincentvbh.github.io/papers/2021-986.pdf).
- NTT Multiplication for NTT-unfriendly Rings.
    - Chi-Ming Marvin Chung, **Vincent Hwang**, [Matthias J. Kannwischer](https://kannwischer.eu), Gregor Seiler, Cheng-Jhih Shih, and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html).
    - TCHES 2021 [paper](https://vincentvbh.github.io/papers/TCHES2021_2_06.pdf) [talk](https://youtube.com/watch?v=a9_-jhD2ZG0) [slide](https://vincentvbh.github.io/slides/TCHES2021_2_06.slide.pdf) [code](https://github.com/ntt-polymul/ntt-polymul) [ePrint](https://vincentvbh.github.io/papers/2020-1397.pdf).
- Polynomial Multiplication in NTRU Prime.
    - Erdem Alkim, Dean Yun-Li Cheng, Chi-Ming Marvin Chung, Hülya Evkan, Leo Wei-Lun Huang, **Vincent Hwang**, Ching-Lin Trista Li, Ruben Niederhagen, Cheng-Jhih Shih, Julian Wälde, and [Bo-Yin Yang](https://homepage.iis.sinica.edu.tw/pages/byyang/index_en.html).
    - TCHES 2021 [paper](https://vincentvbh.github.io/papers/TCHES2021_1_09.pdf) [talk](https://youtube.com/watch?v=F95gXPfXrBA) [slide](https://vincentvbh.github.io/slides/TCHES2021_1_09_slide.pdf) [code](https://github.com/vincentvbh/NTRUPrime-PolyMul) [ePrint](https://vincentvbh.github.io/papers/2020-1216.pdf).





# Notes
- [Fast Fourier Transforms](./FFT.html)
- [Sorting Algorithms and Graph Entropy](./sort.html)

