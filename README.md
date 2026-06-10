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
