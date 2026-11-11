# Datasets


## Toy data 

https://github.com/glouppe/exomini


## PTR4 Physical models

Rows of all datasets are the same models in the same order.

Parameter names are the same as in the retrieval and the truth files:
- **18 parameters**: T_bottom, PTslope_1-5, log_g, M/H, C/O, sigma_lnorm, then for MgSiO3(s) and Fe(s) each log_cloud_radius, log_X_cb_, log_Pbase_, f_sed_.
- **28 parameters**: planet_radius (cm), T_bottom, PTslope_1-10, log_g, M/H, C/O, CO2_mfr, 12C-160__HITEMP_mfr, H20_mfr, CH4_mfr, log_sigma_lnorm_offset, then for Fe(s) and MgSiO3(s) each log_cloud_radius, f_sed, log_X_cb_, log_Pbase_.


| name | shape | type | content |
| --- | --- | --- | --- |
| `features` | (N, n_free) | float64 | physical parameter values, i.e. the "$\theta$" for SBI |
| `cube` | (N, n_free) | float64 | the same points in the unit cube [0, 1] (prior CDF) |
| `models` | (N, 249) | float32 | noiseless spectra at R=100, binned to the WISE1049B points |
| `wavelengths` | (249,) | float64 | $\mu$m, increasing |
| `snr` | (249,) | float64 | WISE1049B S/N per point |
| `models_native` | (N, 501) | float32 | the same models at the native R200 |
| `wavelengths_native` | (501,) | float64 | $\mu$m, increasing |
| `status` | (N,) | uint8 | 1 = ok, 2 = failed (spectra NaN), 0 = not computed yet |
| `prior_bounds` | (n_free, 2) | float64 | min and max of each prior |
| `prior_q10_q90` | (n_free, 2) | float64 | 10% and 90% quantiles of each prior|
