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
The nimbus software requires a prior_samples.txt and ZTF_fields.pkl file commonly over any event analyzed.
The prior_samples.txt file can be found in this repository. They are generated using numpy.random.uniform() function. It is a file where each column is a pair of (magnitude $M$, evolution rate $\alpha$). In this case, 2000 prior values were used for each event analysis.
The ZTF_fields.pkl file gives information about the ipix value for each field, the $E(B-V)$, and the extinction values for ZTF filter: g, r, and i.
