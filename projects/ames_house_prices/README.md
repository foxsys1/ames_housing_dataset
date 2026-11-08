# Ames House Price Prediction

This project predicts Ames, Iowa house sale prices using a scikit-learn preprocessing pipeline and XGBoost.

## Contents

- `notebooks/module1ames.ipynb` - exploratory analysis, preprocessing, cross-validation, and modeling
- `data/` - local training and test data; CSV files are intentionally ignored by Git

The target is log-transformed with `np.log1p`, and model performance is evaluated with RMSE in log space, which is equivalent to RMSLE on the original prices.

## Iterations

- In the first commit, i used a simple XGRegressor model and imputed the null values in categorical and ordinal columns as if they meant the data was missing (most_frequent). I got an improvement of around 44% from the baseline (Dummy prediction using the mean of the target column).
- In the second commit, i made a dedicated preprocessor to register null values on certain columns as semantically meaningful absence. I based this off the documentation from kaggle. I got a very tiny improvement, only around 1% compared to my first commit. 
