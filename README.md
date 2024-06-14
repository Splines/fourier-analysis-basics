<div align="center">
    <h3 align="center"><strong>The basics of Fourier analysis</strong></h3>
    <p>
        A project by Dominic Plein <a href="https://youtube.com/@splience">@Splience</a> & Felix Lentze<br>in the course of a seminar on <a href="https://matematiflo.github.io/SoSe_2024/CompAssistedMath2024.html">computer-assisted maths</a>.
    </p>
    <a href="./src/fourier.ipynb">Jupyter notebook</a>
    | <a href="https://youtube.com/@splience">YouTube Video (TODO)</a>
</div>

<br>


## Abstract

**In this project, we will discuss what sound is, how to represent it mathematically & in a computer, and how to examine its frequency content using Fourier analysis. We will use SageMath along the way for the implementation and for interactive plots.** [SageMath](https://www.sagemath.org/) is a free open-source computer algebra system as superset of Python which bundles many great libraries like `numpy`, `scipy`, `matplotlib`, and more. In the frequency domain, we can manipulate the frequency spectrum of a sound as will be demonstrated by implementing a rudimentary low-pass filter to cut off high frequencies of a square wave signal.

This projected is intended for educational purposes, i.e. we don't focus on performance of our code (for that, see the FFT algorithm implemented in system-level languages like Rust or C++). Basic knowledge of linear algebra as well as Python are required. The key points are explained next to the code. The reader is encouraged to experiment with the code and the provided sound samples.

> [!TIP]
> Throughout your journey of exploring the amazing world of Fourier in this notebook, you might want to have **the amazing book [Linear algebra, signal proceessing, and wavelets. A unified approach](https://www.uio.no/studier/emner/matnat/math/nedlagte-emner/MAT-INF2360/v15/kompendium/) by Øyvind Ryan** open next to you. When we reference a theorem/definition from this book, we refer to the January 21, 2015 Python edition.


## Installation of SageMath (via conda-forge)

> [!WARNING]  
> In order to execute the cells in the Jupyter notebook, you will have to install a SageMath kernel.

SageMath offers a [great installation guide](https://doc.sagemath.org/html/en/installation/) for different OS. SageMath bundles a huge amount of different packages under one umbrella. This can make it a bit tricky to install. Luckily, for macOS and Linux (including WSL, the Windows Subsystem for Linux), we have Conda. [Conda](https://conda.org/) is a multi-platform package management ecosystem. Community-led distributions are available via [conda-forge](https://conda-forge.org/), including SageMath.

So, the only real thing you need is a working conda-forge installation. As [described here](https://doc.sagemath.org/html/en/installation/conda.html), you can install Miniforge, a conda-forge distribution. First, download it:

```bash
curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
```

Then, run the script to install it:

```bash
bash Miniforge3-$(uname)-$(uname -m).sh
```

After that, create a new conda environment containing SageMath. (Note that [mamba](https://mamba.readthedocs.io/en/latest/index.html) is a package manager that serves as a faster drop-in replacement for `conda`. It comes pre-installed with Miniforge.)

```script
mamba create -n sage sage python=3.11
```

This will download many packages, so it might take a while. It's also very big (it will install ~350 packages corresponding to ~1GB in size). Also feel free to use another Python version if you prefer.

After that, activate the new environment:

```bash
mamba activate sage
```

Now you can run `sage` to access the SageMath REPL that you can interact with in the terminal. But your commands won't get persisted, so a Jupyter Notebook might be a better choice. Read on if you want to use SageMath in Jupyter Notebooks inside VSCode.

### Usage of Sage in Jupyter Notebooks in VSCode

The widespread editor [VSCode](https://code.visualstudio.com/) (Visual Studio Code) has great support for Jupyter notebooks via the [Jupyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) (more than 77 Mio. people have already installed it as of April 2024).

The Jupyter extension itself does _not_ provide a kernel for SageMath, but if you followed along with the installation above, you've already created a working conda environment. VSCode will recognize this and shows you [an option](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_create-or-open-a-jupyter-notebook) in a Jupyter Notebook to select the SageMath kernel. And that's it, now you can work with SageMath in a Jupyter Notebook locally in VSCode 🎉

If SageMath does not appear in the kernel list, try to restart VSCode (`Ctrl + Shift + P` to open the command palette, then type in "Reload" and click on "Reload Window"). You may also want to refer to [the official guide](https://doc.sagemath.org/html/en/installation/launching.html#using-jupyter-notebook-through-visual-studio-code-vs-code-in-wsl). Rebooting your computer might also help.

#### Tips to get the most out of SageMath in Jupyter Notebooks in VSCode

You might want to add

```py
from sage.all import *
```

at the beginning of the Jupyter notebook. This way, you will get proper IntelliSense including autocompletion. For example, write `ma` and press `Ctrl + Space` and you will see the available options, e.g. `matrix()`. Note that after first importing all modules, it might take a few seconds for IntelliSense to correctly work and recognize your commands.

If a cell outputs LaTeX code, but you rather see something like `\(\displaystyle \left(\begin{array}{rrr}` etc., you can change the cell output presentation to LaTeX by clicking on the three `...` next to a cell, then `Change Presentation` and choose `text/latex`. LaTeX in markdown cells should work out of the box.

If you prefer to use a JupyterNotebook in the browser, open the terminal (`Ctrl + J` in VSCode), activate sage via `mamba activate sage`, then run `sage -n jupyter`. Your browser will open with a Jupyter Notebook running SageMath and you will see your local files. But this shouldn't have any advantages over the Jupyter Notebook experience in VSCode.



## License

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/Splines/fourier-analysis-basics">The basics of Fourier Analysis</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://github.com/splines">Dominic Plein</a> & Felix Lentze is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-SA 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" alt=""></a></p>
