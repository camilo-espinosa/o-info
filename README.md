# o-info

This repository contains example Jupyter notebooks demonstrating the use of the [`thoi`](https://github.com/Laouen/THOI) library.

## Data

The example data used in these notebooks consists of fMRI recordings from non-human primates under six different brain states: awake, low-dose propofol, high-dose propofol, ketamine, low-dose sevoflurane, and high-dose sevoflurane. The brain was parcellated into 82 regions, and each region contains 500 time samples. The dataset itself is not shared, but the analysis results are displayed within the notebooks as example.

## Notebooks

### 1. `whole_brain.ipynb`

Calculates the four informational measures — DTC, TC, O-Information, and S-Information — for each subject and brain state. The computations are based on the full set of 82 parcellated brain regions.

### 2. `simulated_annealing.ipynb`

Demonstrates the use of simulated annealing to find subsets of regions (n-plets) that maximize or minimize a custom metric — in this case, Cohen’s d — between two states (e.g., awake vs. high-dose propofol).

### 3. `simulated_annealing_awake_vs_rest.ipynb`

Extends the previous approach by comparing the awake state to a weighted sum of all anesthetized states. It identifies n-plets of varying sizes (can take from 3 up to 81) that show the strongest differences according to the selected metric.

Each notebook produces a `pandas` DataFrame to summarize and display the results.

## Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

**Note:** You must install a compatible version of **PyTorch with CUDA support** to enable GPU acceleration. Refer to the [official PyTorch installation guide](https://pytorch.org/get-started/locally/) for instructions based on your system and CUDA version.
