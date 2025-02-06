# Trained Models

This folder contains serialized versions of all trained models for this project, saved using [**joblib**](https://joblib.readthedocs.io/en/latest/). Each file corresponds to a specific model or model type. Storing them here allows for easy loading at inference time without the need for retraining.

## Files Overview

- **`ridge_regression.pkl`**  
  Trained Ridge Regression model.  

- **`lasso_regression.pkl`**  
  Trained Lasso Regression model.  

- **`random_forest.pkl`**  
  Trained Random Forest model.

- **`arma_model.pkl`**  
  Trained ARMA (AutoRegressive Moving Average) model.

- **`neural_network.pkl`**  
  Trained Neural Network model.

## How to Use

1. **Clone/Download the Repository**  
   Ensure you have the full repository so that relative paths to this folder are maintained.

2. **Load Models with joblib**  
   ```python
   import joblib

   # Example: loading the Ridge Regression model
   model = joblib.load("trained_models/ridge_regression.pkl")
   predictions = model.predict(your_input_data)

