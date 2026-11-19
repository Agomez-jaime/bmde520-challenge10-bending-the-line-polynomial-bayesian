# Bending the Line: Polynomial and Bayesian Models on Brain Data

BMDE 520, McGill University — Challenge 10.

Adds non-linearity the classical way, with **polynomial feature expansion**, and handles the resulting explosion in features with regularisation and compression.

Every challenge in this series uses the same setup: 100 OASIS-1 subjects,
gray-matter density averaged inside brain-atlas regions, **Part A** predicting
sex (classification) and **Part B** predicting age (regression, Craddock
parcellations at up to 43 resolutions).

## What's here

**Part A — sex classification (tasks 1–5)**
- Polynomial degree sweeps with linear classifiers and with **Bayesian ridge** (thresholding the continuous prediction back to a class).
- k-means and Gaussian-mixture compression (1–20 components) before the polynomial step.
- Wall-clock **training time** as degree grows, which is why degrees stop at 3.

**Part B — age regression (tasks 6–10)**
- Polynomial **ridge** (degrees 1–5 on 50 features) and Bayesian ridge for age.
- k-means and GMM + polynomial ridge, and the matching timing analysis.

## Files

- `challenge10_andrea_gomez.ipynb` — the full notebook with outputs and plots.

## Data (not included)

Uses **OASIS-1** voxel-based morphometry gray-matter maps (fetched with
`nilearn.datasets.fetch_oasis_vbm`, subject to OASIS's
[data usage agreement](https://sites.wustl.edu/oasisbrains/)), the
**Schaefer 2018** atlas (`fetch_atlas_schaefer_2018`) and the **Craddock
2011/2012** parcellations. None of them are redistributed here; the notebook's
first cells show how each is fetched.

## Author

Andrea Paola Gómez Jaime
