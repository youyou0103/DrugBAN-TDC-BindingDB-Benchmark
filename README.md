\# DrugBAN-TDC-BindingDB-Benchmark



A benchmarked reimplementation of DrugBAN on TDC BindingDB datasets for drug-target interaction / affinity prediction.



\## Project Overview

This repository is built to demonstrate my work on deep learning based drug-target interaction prediction under standardized TDC benchmark settings.



The current project includes experiments on:

\- BindingDB random split

\- BindingDB cold-drug split

\- BindingDB scaffold split

\- PD-specific downstream dataset



\## Tech Stack

\- Python

\- PyTorch

\- TDC

\- RDKit

\- NumPy / Pandas / Scikit-learn



\## Main Results



| Setting | Val AUC | Test AUC | Test AUPR |

|---|---:|---:|---:|

| BindingDB\_random | 0.9316 | 0.9186 | 0.7392 |

| BindingDB\_cold\_drug | 0.8609 | 0.9173 | 0.6883 |

| BindingDB\_scaffold | 0.8758 | 0.8026 | 0.4984 |

| PD | 0.9266 | 0.8967 | 0.8885 |



\## Split Understanding

\- Random split reflects standard i.i.d. evaluation performance.

\- Cold-drug split focuses on generalization to unseen compounds.

\- Scaffold split is more challenging because it evaluates generalization across novel molecular scaffolds.

\- The PD dataset is used for disease-oriented downstream validation.



\## Repository Structure

\- `README.md`: project description

\- `results/metrics\_summary.csv`: main benchmark results



\## Note

This repository focuses on standardized benchmarking and engineering demonstration under the TDC pipeline, rather than strict numerical reproduction of the original paper under its exact original setup.

