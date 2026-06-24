# ML-Guided Genetic Algorithm for 1D Bin Packing Optimization

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Machine Learning](https://img.shields.io/badge/ML-XGBoost-orange)
![Optimization](https://img.shields.io/badge/Optimization-Genetic%20Algorithm-green)
![Research](https://img.shields.io/badge/Project-Research-purple)


## Overview

This project proposes a hybrid optimization framework combining Genetic Algorithms (GA) with Machine Learning techniques to improve the solving process of the 1D Bin Packing Problem (1D-BPP).

The approach addresses two major limitations of standard Genetic Algorithms:

- Poor initial population quality caused by random initialization.
- Premature convergence caused by loss of population diversity.

Two machine learning components are integrated inside the GA:

1. **XGBoost-based population initialization**
   - Learns item ordering patterns from synthetic instances.
   - Generates high-quality initial individuals close to FFD solutions.

2. **Online ML-based fitness sharing**
   - Uses an incremental SGDClassifier.
   - Detects similarity between individuals and penalizes excessive convergence.


## Methodology

The proposed hybrid architecture:
BPP Instance
|
v
XGBoost Ranking Model
|
v
ML-guided Initial Population
|
v
Genetic Algorithm
|
+--> Online Fitness Sharing
|
v
Best Packing Solution

## Key Features

- Genetic Algorithm solver for 1D Bin Packing
- XGBoost-based ranking model for population initialization
- Online learning fitness sharing mechanism
- Adaptive diversity preservation
- Benchmark evaluation and ablation study
- Statistical validation using Wilcoxon signed-rank tests


## Experimental Results

Evaluation was performed on:

- Scholl N3 benchmark instances
- Falkenauer benchmark instances

The hybrid approach achieved:

- Mean Gap reduction from **9.56% → 7.07%**
- Improved convergence behavior
- Better robustness compared to baseline GA
- Only **+16% runtime overhead**


## Technologies

- Python
- NumPy
- Scikit-learn
- XGBoost
- SciPy
- Matplotlib


## Project Structure

ml-guided-genetic-bin-packing/

├── README.md

├── ML_Guided_GA_BinPacking.ipynb

├── data/

│ └── benchmark/

│ └── falkenauer/

└── paper.pdf
