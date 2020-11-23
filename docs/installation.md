# Installation

At the moment, we provide a Python-based library to access and run our models. In the future, we will make our models available through web applications.

Make sure to have [Conda](example.com) and [Git](example.com) installed in your computer. Most likely you do :)

## Install Conda

## Install RDKit

```bash
conda install -c conda-forge rdkit
```

## Install Biopython

```bash
conda install -c conda-forge biopython
```

## Install Git and GitHub

First, make sure that [conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/) is installed.

Create a conda environment and activate it.

```bash
conda env create -f environment.yml
```

```bash
conda env export > environment.yaml
```

```bash
conda create -n ersilia python=3.8
conda activate ersilia
```
Then, simply clone our repository
```bash
gh repo clone ersilia-os/ersilia
```
Visit the cloned directory and install the library using pip:
```bash
cd ersilia
pip install .
```
