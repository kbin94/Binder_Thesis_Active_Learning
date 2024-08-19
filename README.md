# Assessing QBC Active Learning Regression for FTIR Spectroscopy in Wood Dating Applications

This repository contains the Data, Code and Software versions for my Master's thesis "Assessing QBC Active Learning Regression for FTIR Spectroscopy in Wood Dating Applications". \
The main focus on this thesis is the application of the active learning approaches Query-by-Committee (QBC) and IDEAL to FTIR spectral data gathered from several wooden samples originating from Austria, Finland, Norway and Poland. \

## Setup of the environment

This code was developed in a conda environment. You can recreate the environment by using the environment_list.txt file:

```
$ conda create --name <env_name> --file environment_list.txt
```

## Dependencies

The main libraries and frameworks used in this project are:

- [**scikit-learn**](https://scikit-learn.org/stable/index.html): Used for implementing machine learning models like Support Vector Regression (SVR) and Random Forest (RF). [[1]](#1)
- [**modAL**](https://modal-python.readthedocs.io/en/latest/): A modular active learning framework for Python, used to implement the Query-by-Committee (QBC) approach. [[2]](#2)
- [**IDEAL**](http://cse.lab.imtlucca.it/~bemporad/ideal/): Inverse-Distance based Exploration for Active Learning. [[3]](#3)

## Contents

**notebooks**: Contains all juypter notebooks created during this thesis and is structured in two main parts:
-  **Part 1**: Focuses on model optimization and validation.
      - `dpsDeriv1200_model_optimization_validation_permutation_importance_workbook.ipynb`
      - `dps1200_model_optimization_validation_permutation_importance_workbook.ipynb`
-  **Part 2**: Explores active learning techniques applied to the models.
      - `active_learning_workbook_QBC_IDEAL.ipynb`

## Structure

**Part 1**:
The notebooks in this part primarily consist of the following structure:
- Data Import
- Separating the data into training and test set
- Scaling
- Hyperparameter Optimization of Support Vector Regression (SVR) and Random Forest (RF) prediction models
- Validating the optimized models on the test set
- Permutation Importance

**Part 2**:
The Active Learning notebook loosely follows this structure:

- Assessment of the importance of certain parameters on the outcome of the Query-by-Committee and the IDEAL approach
- Comparison to random sampling
- Comparison to a representative supervised machine learning model
- Comparison of QBC and IDEAL

All of the steps above are performed with SVR and RF!

## References

<a id="1">[1]</a> 
F. Pedregosa, G. Varoquaux, A. Gramfort, V. Michel, B. Thirion, O. Grisel,
M. Blondel, P. Prettenhofer, R. Weiss, V. Dubourg, J. Vanderplas, A. Passos,
D. Cournapeau, M. Brucher, M. Perrot, and E. Duchesnay, “Scikit-learn: Machine learning in Python,” Journal of Machine Learning Research, vol. 12, pp. 2825–2830,
2011. [Link](https://jmlr.csail.mit.edu/papers/v12/pedregosa11a.html)

<a id="2">[2]</a> 
T. Danka and P. Horvath, “modAL: A modular active learning framework for Python,” pp. 1–6, 2018. *arXiv preprint arXiv:1805.00979*. [Link](https://arxiv.org/abs/1805.00979)

<a id="3">[3]</a> 
 A. Bemporad, "Active Learning for Regression by Inverse Distance Weighting," arXiv eprint 2204.07177, 2022. [Link](https://arxiv.org/abs/2204.07177)

## Licence

This repository is licensed under the GNU General Public License v3.0. You may use, distribute, and modify this code under the terms of the GPL-3.0 license.

## Author

Karin Binder 200958[at]fhwn.ac.at
