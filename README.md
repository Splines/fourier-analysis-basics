<div align="center">
    <h3 align="center"><strong>The basics of Fourier analysis</strong></h3>
    <p>
        A project by Dominic Plein <a href="https://youtube.com/@splience">@Splience</a> & Felix Lentze<br>in the course of a seminar on <a href="https://matematiflo.github.io/SoSe_2024/CompAssistedMath2024.html">computer-assisted maths</a>.
    </p>
    <a href="./src/fourier.ipynb">Jupyter notebook</a>
    | <a href="https://youtube.com/@splience">YouTube Video (TODO)</a>
</div>

<br>


### Abstract

**In this project, we will discuss what sound is, how to represent it mathematically & in a computer, and how to examine its frequency content using Fourier analysis. We will use SageMath along the way for the implementation and for interactive plots.** [SageMath](https://www.sagemath.org/) is a free open-source computer algebra system as superset of Python which bundles many great libraries like `numpy`, `scipy`, `matplotlib`, and more. In the frequency domain, we can manipulate the frequency spectrum of a sound as will be demonstrated by implementing a rudimentary low-pass filter to cut off high frequencies of a square wave signal.

This projected is intended for educational purposes, i.e. we don't focus on performance of our code (for that, see the FFT algorithm implemented in system-level languages like Rust or C++). Basic knowledge of linear algebra as well as Python are required. The key points are explained next to the code. The reader is encouraged to experiment with the code and the provided sound samples.

Throughout your journey of exploring the amazing world of Fourier in this notebook, you might want to have **the amazing book [Linear algebra, signal proceessing, and wavelets. A unified approach](https://www.uio.no/studier/emner/matnat/math/nedlagte-emner/MAT-INF2360/v15/kompendium/) by Øyvind Ryan** open next to you. When we reference a theorem/definition from this book, we refer to the January 21, 2015 Python edition.


### License

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/Splines/fourier-analysis-basics">The basics of Fourier Analysis</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://github.com/splines">Dominic Plein</a> & Felix Lentze is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-SA 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" alt=""></a></p>
