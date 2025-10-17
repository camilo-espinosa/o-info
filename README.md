# o-info

This repository contains example Jupyter notebooks demonstrating the use of the [`thoi`](https://github.com/Laouen/THOI) library.

## Data

The example data used in these notebooks consists of fMRI recordings from non-human primates under six different brain states: awake, low-dose propofol, high-dose propofol, ketamine, low-dose sevoflurane, and high-dose sevoflurane. The brain was parcellated into 82 regions, and each region contains 500 time samples. The dataset itself is freely available data from [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10572216.svg)](https://zenodo.org/records/10572216); related article: [https://doi.org/10.1371/journal.pone.0314598](https://doi.org/10.1371/journal.pone.0314598).


## Notebooks

### 1. `demo_thoi.ipynb`

Examples for the main functions of the thoi library

### 2. `simulated_annealing.ipynb`

Demonstrates the use of simulated annealing to find subsets of regions (n-plets) that maximize or minimize a custom metric — in this case, Cohen’s d — between two states (e.g., awake vs. non responsive).

## Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

**Note:** You must install a compatible version of **PyTorch with CUDA support** to enable GPU acceleration. Refer to the [official PyTorch installation guide](https://pytorch.org/get-started/locally/) for instructions based on your system and CUDA version.
