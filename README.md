# Evaluating the Statistical Significance of Grid Search Optimization in Support Vector Regression for Dengue Forecasting Using Nested Time-Series Cross-Validation

This repository contains the official implementation, source code notebooks, and datasets for the manuscript submitted to the **Cureus Journal of Computer Science**. 

The study rigorously evaluates whether exhaustive grid-search hyperparameter optimization yields statistically significant predictive enhancements for Support Vector Regression (SVR) in weekly dengue case forecasting when compared against default-hyperparameter configurations.

## Repository Structure

Based on the uploaded experimental artifacts, the repository maintains the following structure:

```text
├── DT.ipynb                   # Decision Tree Baseline Pipeline
├── LR.ipynb                   # Linear Regression Baseline Pipeline
├── RF.ipynb                   # Random Forest Baseline Pipeline
├── SVR.ipynb                  # Core Support Vector Regression Pipeline (Default vs. Grid-Tuned)
├── XGB.ipynb                  # XGBoost Baseline Pipeline
├── dengue_features.xlsx       # Environmental and meteorological training features
├── dengue_features_test.xlsx  # Environmental and meteorological testing features
├── dengue_labels_train.xlsx   # Ground truth weekly dengue case counts for training
└── README.md                  # Comprehensive repository documentation

## Dataset Specifications
The experiments utilize the benchmark dataset from the DengAI: Predicting Disease Spread competition distributed by DrivenData. The dataset encompasses weekly reported dengue case counts and 24 environmental covariates (meteorological measurements, station temperatures, and vegetation indices) for San Juan, Puerto Rico, and Iquitos, Peru, spanning from 1990 to 2013.

- Data Source                   # https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/

## Experimental Environment & Dependencies
To ensure absolute computational determinism and reproducibility, the experiments were executed using Python 3.10+ with the following primary software stack:
  1. scikit-learn (For SVR, PCA, and standard preprocessing validation transformers)
  2. xgboost (For the gradient boosting baseline implementation)
  3. pandas & openpyxl (For processing the structural .xlsx data matrices)
All wall-clock computational overhead benchmarks recorded in the manuscript (averaging 11 to 15 seconds for exhaustive tuning) were evaluated on a local computational workstation equipped with an Intel Core i7-12700H processor and 16 GB of RAM, running a Windows 11 Pro operating system environment.

## Methodological Core Features
  1. Leakage-Free Preprocessing: To prevent forward-looking data leakage, all preprocessing steps (including median imputation, Z-score outlier filtering, standardization, and PCA) are strictly fitted exclusively on the inner training partitions of each split before transforming validation/test boundaries.
  2. Decoupled Validation Logic: The main evaluation utilizes a rigorous nested time-series cross-validation framework to completely isolate inner-loop parameter tuning from outer-loop generalization error estimation.

## Citation
If you utilize this codebase, the pipeline architectures, or the empirical findings in your research, please cite our definitive peer-reviewed paper:

Caesarizky OY, Ilham A, Khikmah L, Madani F: Evaluating the Statistical Significance of Grid Search Optimization in Support Vector Regression for Dengue Forecasting Using Nested Time-Series Cross-Validation. Cureus J Comput Sci. 2026. DOI: [Pending Publisher Assignment]
