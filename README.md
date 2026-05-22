**DrugBAN-TDC-BindingDB-Benchmark**

A benchmark-oriented reimplementation and adaptation of DrugBAN for drug–target interaction prediction under TDC-style BindingDB settings.



**Overview**

This repository is built to present my benchmark and application work based on the DrugBAN framework for drug–target interaction / affinity prediction.



**The current project includes experiments on:**

BindingDB random split
BindingDB cold-drug split
BindingDB scaffold split
PD-specific downstream evaluation



**This repository is mainly intended to demonstrate:**

paper reproduction ability
deep learning engineering ability
split-based generalization analysis
disease-oriented downstream validation
Relation to the Official DrugBAN Repository



**This project is based on the official DrugBAN implementation:**

Original paper:
Interpretable bilinear attention network with domain adaptation improves drug–target prediction
Official repository:
https://github.com/peizhenbai/DrugBAN

The original DrugBAN work was proposed by Bai et al. and published in Nature Machine Intelligence.



**Compared with the official implementation, this repository focuses on:**

standardized benchmark organization under my current experimental pipeline
evaluation on BindingDB with multiple split settings
downstream validation on a Parkinson’s disease (PD) dataset
engineering-oriented result organization for reproduction and analysis
My Contributions



**My work in this repository mainly includes:**

reorganizing and adapting the DrugBAN framework for my current TDC-style BindingDB benchmark setting
conducting experiments under random, cold-drug, and scaffold split settings
performing downstream validation on a PD-specific dataset
summarizing benchmark results and generalization performance under different evaluation protocols
organizing the project into a reproducible and presentation-oriented repository for engineering demonstration


**Main Results**
Setting	Val AUC	Test AUC	Test AUPR
BindingDB\_random	0.9316	0.9186	0.7392
BindingDB\_cold\_drug	0.8609	0.9173	0.6883
BindingDB\_scaffold	0.8758	0.8026	0.4984
PD	0.9266	0.8967	0.8885


**Split Understanding**
Random split reflects standard i.i.d. evaluation performance.
Cold-drug split evaluates generalization to unseen compounds.
Scaffold split is more challenging because it evaluates generalization across novel molecular scaffolds.
PD is used as a downstream disease-oriented validation scenario.


**Environment**

The current implementation is based on:

Python 3.8
PyTorch 1.7.1
DGL 0.7.1
DGLLife 0.2.8
RDKit
NumPy / Pandas / Scikit-learn
YAML-based configuration



Please refer to requirements.txt for the main dependencies.



**How to Run**
Install dependencies: pip install -r requirements.txt
Check experiment configurations under: configs/
Run training / evaluation: python main.py
Repository Structure
main.py: main training / evaluation entry
trainer.py: training and evaluation pipeline
models.py: model definitions
ban.py: bilinear attention related modules
dataloader.py: dataset loading and preprocessing
utils.py: utility functions
configs.py: configuration helper
configs/: YAML experiment configuration files
results/: summarized benchmark results


**Notes**

This repository is not intended as a strict numerical reproduction of the original DrugBAN paper under its exact original experimental setup.



**Instead, this repository focuses on:**

benchmark adaptation under my current data pipeline
engineering-oriented reproduction and organization
split-based performance comparison
downstream disease-oriented validation
License and Attribution



This repository includes code adapted from the official DrugBAN implementation.

The original DrugBAN repository is released under the MIT License.
Please retain the original license text and copyright notice in this repository.



**Acknowledgement**

This work is based on the official DrugBAN implementation and its corresponding paper.

If you find the original DrugBAN work useful, please cite:

Bai, P., Miljković, F., John, B. and Lu, H.
Interpretable bilinear attention network with domain adaptation improves drug-target prediction.
Nature Machine Intelligence (2023).
DOI: 10.1038/s42256-022-00605-1

