# Processed Data

This folder contains processed datasets used for training and evaluating models in the project. The datasets are sequentially processed through multiple notebooks, with each step refining and transforming the data for different modeling approaches.

## Contents & Processing Steps

### Data Cleaning (Notebook `01_data_preparation.ipynb`)
- **`all_cleaned_data.csv`** – The dataset after merging and handling missing values.

### Feature Engineering & Preprocessing (Notebook `02_preprocessing_plus.ipynb`)
- **`filtered_data.csv`** – The complete dataset after applying seasonal mean imputation on missing values and rolling mean values on outliers (on test and train data separately), creating lagged features and shifting the target variable.
- **`final_train_data.csv`** – The training set extracted after splitting (before 2018 vs. after 2018).
- **`final_test_data.csv`** – The test set extracted after splitting (before 2018 vs. after 2018).

### Transformations (Notebook `03_transformations.ipynb`)
- **`log_filtered.csv`** – The dataset after log transformation.
- **`log_train.csv`** – The training set after log transformation.
- **`log_test.csv`** – The test set after log transformation.
- **`testdata_nn_rf.csv`** – The final standardized test set for **Random Forest & Neural Networks**, containing time indices and cyclical transformations.
- **`traindata_nn_rf.csv`** – The final standardized training set for **Random Forest & Neural Networks**, containing time indices and cyclical transformations.

### Deseasonalization & Detrending (Notebook `04_deseasonalization_detrending.ipynb`)
- **`seasonality_components.csv`** – Extracted seasonal components from water levels.
- **`train_detrended.csv`** – The detrended and deseasonalized training set, used for **ARMA & Linear Regression**.
- **`test_detrended.csv`** – The detrended and deseasonalized test set, used for **ARMA & Linear Regression**.

