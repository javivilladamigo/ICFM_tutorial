# Tutorial on Iterative Generative Unfolding with CFMs for the PHYSTAT 2024 Conference on Unfolding
This repository is a small tutorial on the use of generative networks (Conditional Flow Matching in this case) for iterative generative unfolding presented at the [PHYSTAT 2024](https://indico.cern.ch/event/1357972/) conference.

CFM [[1](https://arxiv.org/abs/2210.02747), [2](https://arxiv.org/abs/2305.10475)] is a network that regresses a velocity field to encode the time evolution between particle-level events and reco-level events. The iterative setup consists on training for the unfolding task on MC and applying it then to Data, after which the MC prior is reweighted to match the Data Unfolded, and repeating. For a thorough description, please see [[3](https://arxiv.org/abs/2212.08674)].

## Setup
To start, let's clone the repository:
```
git clone https://github.com/javivilladamigo/ICFM_tutorial.git
cd ICFM_tutorial/
```
It is also recommended to create a python environment via:
```
python -m venv ICFM_venv
source ICFM_venv/bin/activate
```
Then, install the required packages via:
```
pip install -r requirements.txt
```
The tutorial can be found inside the notebook unfolding_tutorial.ipynb.
## Data
The data used for this tutorial is, just as for the [OmniFold tutorial](https://github.com/ftoralesacosta/OMNIFOLD_Tutorial/), a [Pythia/Herwig + Delphes Jet Datasets for OmniFold Unfolding](https://zenodo.org/records/3548091). To load the data, one can simply use the [energyflow python pacakge](https://energyflow.network/docs/datasets/#z-jets-with-delphes-simulation). This tutorial only looks at a subset of simulators and observables, but you can refer to the website for a full documentation of the data inside the files.
If you use this dataset, please cite the Zenodo record as well as the corresponding paper: A. Andreassen, P. T. Komiske, E. M. Metodiev, B. Nachman, J. Thaler, OmniFold: A Method to Simultaneously Unfold All Observables, [arXiv:1911.09107](https://arxiv.org/abs/1911.09107).
