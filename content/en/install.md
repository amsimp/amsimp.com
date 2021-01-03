---
title: Installing AMSIMP
sidebar: false
---

If you don't have Python yet and want the simplest way to get started, we recommend you use the [Anaconda Distribution](https://www.anaconda.com/distribution) - it includes Python, NumPy, and some of the other necessary packages to successfully install and run the software.

AMSIMP can be installed with `conda`, or with `pip`. For more detailed instructions, consult our [Python and AMSIMP installation guide](#python-amsimp-install-guide) below.

## conda

Before installation via this particular method, TensorFlow needs to be installed through the Python Package Index (PyPI)
using the following command:

```bash
pip install tensorflow
```

AMSIMP is distributed on [Anaconda Cloud](https://anaconda.org/amsimp/amsimp>) and can be installed using conda:

```bash
conda install -c amsimp amsimp
```

If you run into any issues, you can either create an issue on [GitHub](https://github.com/amsimp/amsimp/issues) or
contact us by [email](support@amsimp.com).

## pip

If you use `pip`, you can install it with:

```bash
pip install amsimp
```

<a name="python-amsimp-install-guide"></a>
# Python and AMSIMP installation guide

Installing and managing packages in Python is complicated, there are a
number of alternative solutions for most tasks. This guide tries to give the
reader a sense of the best (or most popular) solutions, and give clear
recommendations.

## Recommendations

On all of Windows, macOS, and Linux:

- Install [Anaconda](https://www.anaconda.com/distribution/) (it installs all
  packages you need and all other tools mentioned below).
- For writing and executing code, use notebooks in
  [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/index.html) for
  exploratory and interactive computing, and
  [Spyder](https://www.spyder-ide.org/) or [Visual Studio Code](https://code.visualstudio.com/)
  for writing scripts and packages.
- Use [Anaconda Navigator](https://docs.anaconda.com/anaconda/navigator/) to
  manage your packages and start JupyterLab, Spyder, or Visual Studio Code.

### Alternative if you prefer pip/PyPI

For users who know, from personal preference, they prefer a pip/PyPI-based solution,
we recommend:
- Install Python from, for example, [python.org](https://www.python.org/downloads/),
  [Homebrew](https://brew.sh/), or your Linux package manager.
- Use [Poetry](https://python-poetry.org/) as the most well-maintained tool
  that provides a dependency resolver and environment management capabilities
  in a similar fashion as conda does.
- If you are installing the software via this method, please ensure you have all of the required dependencies prior to installation. You will also need to have a C compiler installed on your machine if you are choosing this method.

Further information about the required dependencies can be found here:

- **Python** 3.7.x (https://www.python.org/)
- **tqdm** (https://tqdm.github.io/) |
  A Fast, Extensible Progress Bar for Python and CLI.
- **NumPy** (https://numpy.org/) |
  Python package for scientific computing including a powerful N-dimensional array object.
- **Astropy** (https://www.astropy.org) |
  A Community Python Library for Astronomy.
- **Iris** (https://scitools.org.uk/iris/docs/latest/) |
  A powerful, format-agnostic, community-driven Python library for analysing and visualising Earth science data.
- **Tensorflow** 2.0 or later (https://www.tensorflow.org) |
  TensorFlow is an end-to-end open source platform for machine learning.
