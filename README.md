# nimbus-on-O4a
This repository contains the codes required and files used to run nimbus on O4a events.

## Events analyzed
The following kilonova events were analyzed using nimbus:
| GCN Event  | P_astro | Coverage fraction |
| ------------- | ------------- | ------------- |
| S230518h | 0.90 | 0.0 |
| GW230529 | 0.93 | 0.07 |
| S230627c | 0.97 | 0.74 |
| S230731an | 0.997 | 0.03 |
| S231113bw | 0.96 | 0.11 |

## Important files needed for nimbus
The `nimbus` software requires a `prior_samples.txt` and `ZTF_fields.pkl` file commonly over any event analyzed.

The `prior_samples.txt` file can be found in this repository. They are generated using `numpy.random.uniform()` function. It is a file where each column is a pair of `(magnitude $M$, evolution rate $\alpha$)`. In this case, $2000$ prior values were used for each event analysis. 

The `ZTF_fields.pkl` file gives information about the `ipix value` for each field, the $E(B-V)$, and the extinction values for `ZTF filter`: `g`, `r`, and `i`.

Other than common files, nimbus requires the following files to calculate the likelihood of the data. These files can be found in the individual directories for each event.

| File | Description |
| ------------- | ------------- |
| `skymap file` | A file in `fits.gz` format that contains the 3-dimensional Gravitational Waves skymap localization information.|
| `data file` | A file in `csv` or `txt` format containing information on the observations in a nimbus-readable format.|

## Extra files generated for smoothness
Some optional files that were generated during the analysis were added to this repository as required.

| File | Description |
| ------------- | ------------- |
| `fields file` | A file in `txt` format that contains the field number of unique observations for an individual event.|
| `status file` | A file in `txt` format containing information on the status of each likelihood calculation job.|
| `nan fields file` | A file in `txt` format containing the field numbers that have 0.0 field probability, leading to the blowing up of integral and no results in likelihood file.|
