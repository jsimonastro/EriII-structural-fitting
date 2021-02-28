# Eridanus II Structural Fitting

by Josh Simon & Alex Drlica-Wagenr

Structural fit to HST imaging of Eridanus II and its central star cluster ([Simon et al. 2021](https://arxiv.org/abs/2012.00043)). This fit uses a binned Poisson maximum-likelihood framework, as described in Appendix C of [Drlica-Wagner et al. (2020)](https://arxiv.org/abs/1912.03302).

## Installation

This Jupyter notebook depends on `numpy`, `matplotlib`, `astropy`, `emcee`, and `corner`. We recommend installing these packages in a `conda` environment with something like this:

```
conda create -n eriII jupyter numpy matplotlib astropy emcee corner
```

Once the environment is installed, you should be able to download (or clone) the notebook and associated data file.

## Viewing

It is possible to view the content of this notebook on the web. If the notebook fails to render on GitHub directly, you can try using [nbviewer](https://nbviewer.jupyter.org/) and shown [here](https://nbviewer.jupyter.org/github/jsimonastro/EriII-structural-fitting/blob/main/mcmc_structural_fit_eri2_final.ipynb)

## Contents of data table

The file eri2.cat containing the HST photometry consists of 7 columns.  Columns 1 and 2 are the X and Y positions in the ACS image, columns 3 and 4 are the magnitudes and uncertainties in the F606W filter (in the STMAG system; https://hst-docs.stsci.edu/acsdhb/chapter-5-acs-data-analysis/5-1-photometry), columns 5 and 6 are the magnitudes and uncertainties in the F814W filter (in the STMAG system), and column 7 is the photometric quality flag.  Flag bits are: 1=fails chi criterion in F606W, 2=fails chi criterion in F814W, 4=fails sharp criterion in F606W, 8=fails sharp criterion in F814W, 16=bright neighbor within 4 pixels, 32=bright neighbor within 8 pixels, 64=bright neighbor within 12 pixels and 2.5 mag, 128=bright neighbor within 16 pixels and 2.5 mag, 256=bright neighbor within 20 pixels and 1.5 mag, 512=bright neighbor within 24 pixels and 1.5 mag, 1024=fails photometric uncertainty criterion in both bands.

In order to convert the pixel positions to equatorial coordinates, the WCS information for the ACS image is:

CD1_1   = -9.7207414806871E-06

CD1_2   = 1.69676173695811E-07

CD2_1   = 1.69676173695811E-07

CD2_2   = 9.72074148068713E-06

CRVAL1  =    56.09056245173978

CRVAL2  =   -43.53022649816447

CRPIX1  =    3951.096595646065

CRPIX2  =    3922.701986935564

CTYPE1  = 'RA---TAN'

CTYPE2  = 'DEC--TAN'

ORIENTAT=   0.9999999999999952                                                  

## Citation

If you use this code, please cite Appendix C of [Drlica-Wagner et al. (2020)](https://arxiv.org/abs/1912.03302) for the maximum likelihood method and [Simon et al. (2021)](https://arxiv.org/abs/2012.00043) for this specific implementation.
