# Australian Weather Prediction: KNN & Feature Selection

This repository implements a robust K-Nearest Neighbors (KNN) classification pipeline to predict next-day rain in Australia, utilizing the historical BOM (Bureau of Meteorology) dataset. 

Developed as part of a Computer Science academic project at Amirkabir University of Technology, this project focuses heavily on domain-aware data imputation, preventing data leakage, and automated feature selection.

##  Key Concepts Explored
* **Domain-Aware Imputation:** Replacing missing weather data using Split-Apply-Combine techniques (grouping by `Location` and `Month` to find accurate medians).
* **Feature Selection:** Utilizing Scikit-Learn's `SequentialFeatureSelector` (SFS) to mathematically identify the 10 most impactful weather variables.
* **Data Leakage Prevention:** Identifying and removing target-derived features (like `RISK_MM`) that artificially inflate model accuracy.
* **Hyperparameter Tuning:** Evaluating $K$ values from 1 to 20 to find the optimal balance between bias and variance.

##  Repository Structure
```text
weather-prediction-knn/
│
├── data/                 
├── weather.ipynb/             # Jupyter notebooks with full ML pipelines
├── .gitignore             # Strict ignore rules for dataset files
└── README.md              # Project documentation