# Ames House Price Prediction

This project predicts Ames, Iowa house sale prices using a scikit-learn preprocessing pipeline and XGBoost.

## Contents

- `notebooks/module1ames.ipynb` - exploratory analysis, preprocessing, cross-validation, and modeling
- `data/` - local training and test data; CSV files are intentionally ignored by Git

The target is log-transformed with `np.log1p`, and model performance is evaluated with RMSE in log space, which is equivalent to RMSLE on the original prices.
