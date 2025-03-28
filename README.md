# Random feature-based double Vovk-Azoury-Warmuth algorithm for online multi-kernel learning

The nummerical results from the paper "Random feature-based double Vovk-Azoury-Warmuth algorithm for online multi-kernel learning" by Dmitry B. Rokhlin and Olga V. Gurtovaya.

## Authors

Dmitry B. Rokhlin
Institute of Mathematics, Mechanics, and Computer Sciences of the Southern Federal University  
Regional Scientific and Educational Mathematical Center of the Southern Federal University  
`dbrohlin@sfedu.ru`

Olga V. Gurtovaya  
Institute of Mathematics, Mechanics, and Computer Sciences of the Southern Federal University  
`imedashvili@sfedu.ru`


## Abstract

We introduce a novel multi-kernel learning algorithm, $\text{VAW}^2$, for online least squares regression in reproducing kernel Hilbert spaces (RKHS). $\text{VAW}^2$ leverages random Fourier feature-based functional approximation and the Vovk-Azoury-Warmuth (VAW) method in a two-level procedure: VAW is used to construct expert strategies from random features generated for each kernel at the first level, and then again to combine their predictions at the second level. A theoretical analysis yields a regret bound of $O(T^{1/2}\ln T)$ in expectation with respect to artificial randomness, when the number of random features scales as $T^{1/2}$. Empirical results on some benchmark datasets demonstrate that $\text{VAW}^2$ achieves superior performance compared to the existing online multi-kernel learning algorithms: Raker and OMKL-GF, and to other theoretically grounded method methods involving convex combination of expert predictions at the second level.

## Setting Up Extra Libraries

To ensure proper functionality, install the `opera` package. It provides algorithms for robust online prediction of time series using expert advice, such as BOA, ML-Prod, and ML-Poly.

Installation instructions are available in the repository: [https://github.com/Dralliag/opera-python/blob/develop/README.md](https://github.com/Dralliag/opera-python/blob/develop/README.md)

**Important:** The Raker and OMKL-GF algorithms used for comparison are located in the `mkl_algorithms.py` file within the following repository: [https://github.com/pouyamghari/Graph-Aided-Online-Multi-Kernel-Learning/blob/main/mkl_algorithms.py](https://github.com/pouyamghari/Graph-Aided-Online-Multi-Kernel-Learning/blob/main/mkl_algorithms.py). Obtain this file to run the comparison.

## Datasets to Download

The following Jupyter notebooks reproduce the results for the specified datasets:

* [`Airfoil.ipynb`](https://archive.ics.uci.edu/ml/datasets/Airfoil+Self-Noise): Reproduces the results associated with the Airfoil dataset.
* [`Bias.ipynb`](https://archive.ics.uci.edu/ml/datasets/Bias+correction+of+numerical+prediction+model+temperature+forecast): Reproduces the results associated with the Bias dataset.
* [`Concrete.ipynb`](https://archive.ics.uci.edu/ml/datasets/Concrete+Compressive+Strength): Reproduces the results associated with the Concrete dataset.
* [`Naval.ipynb`](https://archive.ics.uci.edu/ml/datasets/Condition+Based+Maintenance+of+Naval+Propulsion+Plants): Reproduces the results associated with the Naval dataset.
* `AR4.ipynb`: Reproduces the results associated with artificial data generated by the AR(4) model:

$$
x_t = \nu_0 x_{t-4} + \nu_1 x_{t-3} + \nu_2 x_{t-2} + \nu_3 x_{t-1} + \epsilon_t, \quad y_t = x_{t+1}, \quad t = 1, ..., 5000,
$$

where $\nu_0 = 0.5$, $\nu_1 = -0.3$, $\nu_2 = 0.2$, $\nu_3 = 0.1$, $\epsilon_t \sim \mathcal{N}(0, 1)$, and $x_k = 0$ for $k = -3, ..., 0$.

## Usage

1.  Download datasets from the UCI Machine Learning Repository (Airfoil, Bias, Concrete, and Naval).
2.  Install the `opera` library.
3.  Obtain the `mkl_algorithms.py` file from the provided repository.
4.  Place datasets and the `mkl_algorithms.py` file in a directory accessible by the Jupyter notebooks.
5.  Run the Jupyter notebooks (`Airfoil.ipynb`, `Bias.ipynb`, `Concrete.ipynb`, `Naval.ipynb`, `AR4.ipynb`) to reproduce results.
