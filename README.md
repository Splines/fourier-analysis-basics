## The basics of Fourier analysis

**_A project by Dominic Plein ([@Splience](https://youtube.com/@splience)) & Felix Lentze_** in the course of the seminar on [computer-assisted mathematics](https://matematiflo.github.io/SoSe_2024/CompAssistedMath2024.html).

> [!NOTE]  
> - [Jupyter notebook](./src/fourier.ipynb)
> - YouTube video (TODO)
> - [Awesome Book: Linear algebra, signal proceessing, and wavelets. A unified approach. By Øyvind Ryan.](https://www.uio.no/studier/emner/matnat/math/nedlagte-emner/MAT-INF2360/v15/kompendium/applinalgpython.pdf)<br>(many different [versions](https://www.uio.no/studier/emner/matnat/math/nedlagte-emner/MAT-INF2360/v15/kompendium/) are available)

**In this project, we will discuss what sound is, how to represent it mathematically & in a computer, and how to examine its frequency content using Fourier analysis. We will use SageMath along the way for the implementation and for interactive plots.** [SageMath](https://www.sagemath.org/) is a free open-source computer algebra system as superset of Python which bundles many great libraries like `numpy`, `scipy`, `matplotlib`, and more. In the frequency domain, we can manipulate the frequency spectrum of a sound as will be demonstrated by implementing a rudimentary low-pass filter to cut off high frequencies of a square wave signal.

This projected is intended for educational purposes, i.e. we don't focus on performance of our code (for that, see the FFT algorithm implemented in system-level languages like Rust or C++). Basic knowledge of linear algebra as well as Python are required. The key points are explained next to the code. The reader is encouraged to experiment with the code and the provided sound samples.

Throughout your journey of exploring the amazing world of Fourier in this notebook, you might want to have **the amazing book [Linear algebra, signal proceessing, and wavelets. A unified approach](https://www.uio.no/studier/emner/matnat/math/nedlagte-emner/MAT-INF2360/v15/kompendium/) by Øyvind Ryan** open next to you. When we reference a theorem/definition from this book, we refer to the January 21, 2015 Python edition.
