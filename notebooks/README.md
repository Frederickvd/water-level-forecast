# Notebooks
This folder contains Jupyter notebooks covering data preprocessing, feature engineering, and model training.

## 📂 Contents:
### **🔹 Preprocessing & Data Preparation**
1. **`01_data_preparation.ipynb`** → Converts raw datasets to CSV, removes unnecessary data, merges features by date, and fills missing values (e.g., forward-fill for weekly groundwater levels).
2. **`02_preprocessing_plus.ipynb`** → 
   - **Preprocessing:** Splits dataset into train/test (before 2018 vs. after 2018), applies seasonal mean imputation on missing values and rolling mean values on outliers.
   - **Feature Engineering:** Creates lagged features (past 7 days), shifts target variable as we predict tomorrow’s water level.

### **🔹 Feature Engineering & Transformation**
3. **`03_transformations.ipynb`** → Applies log transformation, standardization, and cyclical encoding of time-related variables to help random forest and neural network capture seasonal patterns and trends.
4. **`04_deseasonalization_detrending.ipynb`** → Removes seasonality and trends for ARMA & Linear Regression models, ensuring stationarity. Detrends climate change data to avoid misleading regression coefficients.

### **🔹 Modeling & Prediction**
5. **`05_linear_regression.ipynb`** → Lasso and Ridge linear regression model on stationary, standardized data.
6. **`06_random_forest.ipynb`** → Random forest model, which learns trends and seasonality directly from features.
7. **`07_arma_model.ipynb`** → ARMA time series model applied to stationary water level data.
8. **`08_neural_network.ipynb`** → Neural network model trained on standardized inputs.

⚠️ *Each notebook follows a sequential process. The final processed datasets can be found in `data/processed/`.*
