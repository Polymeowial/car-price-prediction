# Predicting used car price using XGBoost

## Overview
This project employs XGBoost to predict used car price as part of a Kaggle competition. The data set can be retrieved [here](https://www.kaggle.com/competitions/act61-mfe-prediction-competition/data).

- Files structure: <br>
The ``Preprocessing`` folder contains scripts for data cleaning, original dataset, cleaned dataset, and utility functions. You dont need to run any files in this folder manually. Simply run the ``Modeling.ipynb`` notebook—this will automatically execute the necessary preprocessing steps.


## Requirements
All Python package dependencies are listed in `requirements.txt`. To install them, run:

```bash
pip install -r requirements.txt
```

## Notebook Summary
Below is the summary for each part in the file ``Modeling.ipynb``


__A. Setups__
- Import necessary libraries and set up visual properties for visualization.

- Execute data cleaning code from ``Preprocessing/Data_Cleaning`` and load the cleaned dataset.

- Split the data into training and test sets.


__B. EDA__

- Use visualizations to identify and exclude predictors with low predictive value.

- Detect and remove outliers from the dataset.


__C. Variable Encoding__
- Drop features with low predictive power (``fuel``, ``seller_type``, ``seat``).
- Standardize high-magnitude features (``km_driven``, ``engine``) to prevent numerical issues.
- Encode ``owner`` as a numeric variable.
- One-hot encode variable ``tranmission`` and ``brand``.


__D. Model Tuning__ <br>
Perform hyperparameter optimization using Bayesian search to find the best model configuration.

__E. Performance Evaluating__ <br>
Evaluate the model performance on test set.