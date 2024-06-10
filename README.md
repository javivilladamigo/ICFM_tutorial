# Tutorial on Iterative Generative Unfolding with CFMs for the PHYSTAT 2024 Conference on Unfolding
This repository is a small tutorial on the use of generative networks (Conditional Flow Matching in this case) for iterative generative unfolding presented at the [PHYSTAT 2024](https://indico.cern.ch/event/1357972/) conference.

CFM [[1](https://arxiv.org/abs/2210.02747), [2](https://arxiv.org/abs/2305.10475)] is a network that regresses a velocity field to encode the time evolution between particle-level events and reco-level events.

## Setup
To start, it is recommended to create a python environment via:
```
python -m venv ICFM_venv
source ICFM_venv/bin/activate
```
Then, install the required packages via:
```
pip install -r requirements.txt
```
## Data
The data is...
