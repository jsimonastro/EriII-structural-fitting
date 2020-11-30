# Eridanus II Structural Fitting

Structural fit to HST imaging of Eridanus II and its central star cluster (Simon et al. 2020). This fit uses a binned Poisson maximum-likelihood framework, as described in Appendix C of [Drlica-Wagner et al. (2020)](https://arxiv.org/abs/1912.03302).

## Installation

This Jupyter notebook depends on `numpy`, `matplotlib`, `astropy`, `emcee`, and `corner`. We recommend installing these packages in a `conda` environment with something like this:

```
conda create -n eriII jupyter numpy matplotlib astropy emcee corner
```

Once the environment is installed, you should be able to download (or clone) the notebook and associated data file.

## Viewing

It is possible to view the content of this notebook on the web. If the notebook fails to render on GitHub directly, you can try using [nbviewer](https://nbviewer.jupyter.org/) and shown [here](https://nbviewer.jupyter.org/github/jsimonastro/EriII-structural-fitting/blob/main/mcmc_structural_fit_eri2_final.ipynb)

## Citation

If you use this code, please cite Simon et al. (2020)
