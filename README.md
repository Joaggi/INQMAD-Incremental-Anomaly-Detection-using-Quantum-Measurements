# InQMAD: Incremental Quantum Measurement Anomaly Detection
This is the official repository for INQMAD. It has been created using Tensorflow and Jax. 

InQMAD is now part of [PySAD](https://github.com/selimfirat/pysad). Check it out!

## Abstract:

Streaming anomaly detection refers to the problem of detecting anomalous data samples in streams of data. This problem poses challenges that classical and deep anomaly detection methods are not designed to cope with, such as conceptual drift and continuous learning. State-of-the-art flow anomaly detection methods rely on fixed memory using hash functions or nearest neighbors that may not be able to constrain high frequency values or remove seamless outliers and cannot be trained in an end-to-end deep learning architecture. We present a new incremental anomaly detection method that performs continuous density estimation based on random Fourier features and the mechanism of quantum measurements and density matrices. The method continuously updates the estimation of the density of normal samples, giving more importance to new samples and decreasing the importance of older samples. It can process potentially endless data and its update complexity is constant O(1). A systematic evaluation against 12 state-of-the-art streaming anomaly detection algorithms and using 12 streaming datasets is presented.

## Published in: 
- 2022 IEEE International Conference on Data Mining Workshops (ICDMW)
## Date of Conference: 
- 28 November 2022 - 01 December 2022
## Date Added to IEEE Xplore: 
- 08 February 2023
## DOI: 
- 10.1109/ICDMW58026.2022.00107
## Conference Location: 
- Orlando, FL, USA 


# Dataset

All the data can be found in https://zenodo.org/records/18613986
Here is an enhanced, clearer, and more professional version of your section. It improves structure, clarity, and reproducibility while keeping it concise and research-oriented.

---

# Dataset

All datasets used in the experiments are publicly available on Zenodo:

🔗 **[https://zenodo.org/records/18613986](https://zenodo.org/records/18613986)**

The Zenodo repository contains:

* Raw datasets used in the paper
* Preprocessed versions (when applicable)
* Metadata and experiment-related files

Please download the datasets and place them in the appropriate directory as expected by the experiment configuration files.

---

# Setup

## Environment Installation

We recommend using **Miniconda** to ensure reproducibility.

### 1️⃣ Install Miniconda

Download and install Miniconda from:
[https://docs.conda.io/en/latest/miniconda.html](https://docs.conda.io/en/latest/miniconda.html)

### 2️⃣ Create the Conda Environment

From the root of the repository, run:

```bash
conda env create -f environment.yml
conda activate learning-with-density-matrices
```

This will create an isolated environment with all required dependencies.

### 3️⃣ Install the Package

Install the project in editable mode:

```bash
pip install -e .
```

If you plan to contribute or run tests, install development dependencies as well:

```bash
pip install -e .[dev]
```

Editable mode (`-e`) ensures that changes to the source code are immediately reflected without reinstalling the package.

---

## Git Submodules

This repository depends on external components managed as **Git submodules**.

After cloning the repository, initialize and update all submodules:

```bash
git submodule update --init --recursive
```

If you already cloned the repository without submodules, you can run the same command to properly fetch them.

---

## Experiment Tracking with MLflow

All experiments are logged using **MLflow** with a local SQLite backend.

### 1️⃣ Create the Tracking Directory

```bash
mkdir -p mlflow
```

Experiments will be stored under:

```
mlflow/tracking.db
```

### 2️⃣ Launch the MLflow UI

After running experiments, start the MLflow dashboard with:

```bash
mlflow ui --port 8080 --backend-store-uri sqlite:///mlflow/tracking.db
```

Then open your browser at:

```
http://localhost:8080
```

The dashboard allows you to:

* Compare experiment runs
* Track metrics and parameters
* Visualize artifacts
* Reproduce results

---

# Citation

If you use this repository in your research, please cite:

```bibtex
@article{gallego2025inqmad,
  title={INQMAD: incremental streaming anomaly detection with density matrices, quantum measurement, and density estimation},
  author={Gallego, Joseph and Bustos-Brinez, Oscar A and Gonz{\'a}lez, Fabio A},
  journal={Neural Computing and Applications},
  volume={37},
  number={32},
  pages={27475--27503},
  year={2025},
  publisher={Springer}
}
```
```bibtex
@dataset{gallego_2026_18613986,
  author       = {Gallego, Joseph and
                  Bustos-Briñez, Oscar Alberto and
                  Gonzalez, Fabio},
  title        = {InQMAD: Incremental Quantum Measurement Anomaly
                   Detection Dataset
                  },
  month        = feb,
  year         = 2026,
  publisher    = {Zenodo},
  version      = {1.0.0},
  doi          = {10.5281/zenodo.18613986},
  url          = {https://doi.org/10.5281/zenodo.18613986},
}
```
```bibtex
@software{joagg_2022_7183564,
  author       = {Joagg},
  title        = {Joaggi/Incremental-Anomaly-Detection-using-
                   Quantum-Measurements: v1.0.0
                  },
  month        = oct,
  year         = 2022,
  publisher    = {Zenodo},
  version      = {v1.0.0},
  doi          = {10.5281/zenodo.7183564},
  url          = {https://doi.org/10.5281/zenodo.7183564},
}
```
We appreciate citations as they help support continued research in density matrix–based machine learning methods.

