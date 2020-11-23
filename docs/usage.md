# Basic usage

> In this quick-start guide, we will run antibiotic activity predictions for small molecule compounds.

The model based on [Stokes et al. Cell, 2020](https://pubmed.ncbi.nlm.nih.gov/32084340/).
Authors kindly shared to the community the model checkpoint, so all we did in Ersilia was to bundle this model for easy deployment.

Models in Ersilia are identified with the following code structure: `eos{digit}{3 alphanumeric characters}`.
You can browse available models from the [Ersilia model hub](https://ersilia-os.github.io/ersilia-hub.github.io/).

Ersilia code for the [antibiotic activity](https://ersilia-os.github.io/ersilia-hub.github.io/first-gemma-post/) model is `eos0aaa`.

## Python console

### Fetch and initialize model

```python
from ersilia import ErsiliaModel
model_id = 'eos0aaa'
em = ErsiliaModel(model_id)
```

What happens behind this code is the following:

1. The model of interest (`eos0aaa`) is fetched from:
    * A [GitHub repository](https://github.com/ersilia-os/eos0aaa) containing, _at least_:
        * A `service.py` script defining the serving class (i.e. the class that will provide predictions)
        * A `pack.py` script that will generate a model bundle for easy deployment, based on [BentoML](https://www.bentoml.ai/)
    * A compressed file, stored at [Open Science Framework (OSF)](https://osf.io/hu3km/) containing model checkpoint files, i.e. the trained parameters of the model
2. A `~/bentoml/repository/eos0aaa/` folder is created containing the bundled model (see BentoML docs for more details)
3. A `pip` package named `eos0aaa` is created in your local computer

The fetching functionalities of Ersilia are configurable. Please see advanced usage cases for more details.

### Run prediction

Once the model is ready, one can simply run predictions for the molecules of interest. Let's say that we want to predict the antibiotic activity of:
The standard input are SMILES strings.

* Ceftazidime: `[O-]C(=O)C1=C(CS[C@]2([H])[C@H](NC(=O)C(=N/OC(C)(C)C(O)=O)\C3=CSC(N)=N3)C(=O)N12)C[N+]1=CC=CC=C1`
* Halicin: `C1=C(SC(=N1)SC2=NN=C(S2)N)[N+](=O)[O-]`
* Ibuprofen: `CC(C)CC1=CC=C(C=C1)C(C)C(O)=O`

```python
smiles = ['[O-]C(=O)C1=C(CS[C@]2([H])[C@H](NC(=O)C(=N/OC(C)(C)C(O)=O)\C3=CSC(N)=N3)C(=O)N12)C[N+]1=CC=CC=C1',
          'C1=C(SC(=N1)SC2=NN=C(S2)N)[N+](=O)[O-]',
          'CC(C)CC1=CC=C(C=C1)C(C)C(O)=O']
em.predict(smiles)
```

## Command-line interface (CLI)

Ersilia models are stored as BentoML bundles. Hence one can use the outstanding functionalities of this library to deploy models.

To fetch a BentoML bundle from our repository using the CLI, simply run:

```
ersilia fetch eos0aaa
```

Now, you can serve predictions the way you wish. BentoML offers a great spectrum of possibilities and Ersilia incorporates all of them.
For example, you can simply run to obtain predictions for the drug Halicin:

```
ersilia predict eos0aaa --input='["C1=C(SC(=N1)SC2=NN=C(S2)N)[N+](=O)[O-]"]'
