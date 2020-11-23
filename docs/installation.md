# Installation

At the moment, we provide a Python-based library to access and run our models. In the future, we will make our models available through web applications.

Make sure to have [Conda]() and [Git]() installed in your computer. Most likely you do :)

## Install Conda

## Install RDKit

```
conda install -c conda-forge rdkit
```

## Install Biopython

```
conda install -c conda-forge biopython
```

## Install Git and GitHub

First, make sure that [conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/) is installed.

Create a conda environment and activate it.

```
conda env create -f environment.yml
```

```
conda env export > environment.yaml
```


```
conda create -n ersilia python=3.8
conda activate ersilia
```
Then, simply clone our repository
```
gh repo clone ersilia-os/ersilia
```
Visit the cloned directory and install the library using pip:
```
cd ersilia
pip install .
```
