# Results

This folder contains the results from our model predictions and evaluations for forecasting water levels in **Lake Constance**.

## 📂 Contents:

## 📁 plots/ → Key visualizations generated during the analysis

### 📁 accuracy/ → Model performance and residuals analysis
- **accuracy_arma.png** → Predicted vs. actual water levels for the ARMA model.
- **accuracy_l_r.png** → Predicted vs. actual water levels for Ridge and Lasso Regression.
- **accuracy_neural_network.png** → Predicted vs. actual water levels for the Neural Network model.
- **accuracy_random_forest.png** → Predicted vs. actual water levels for the Random Forest model.
- **residual_dist_l_r.png** → Distribution of residuals for Ridge and Lasso Regression.

### 📁 feature_importance/ → Feature importance rankings for different models
- **feature_imp_lasso.png** → Feature importance for the Lasso Regression model.
- **feature_imp_ridge.png** → Feature importance for the Ridge Regression model.
- **feature_imp_random_forest.png** → Feature importance for the Random Forest model, excluding the first lag.
- **feature_imp_neural_network.png** → Feature importance for the Neural Network model, excluding the first lag.

- **📁 metrics/** → Evaluation metrics for model performance
  - `model_performance.csv` → RMSE, MSE, and other evaluation metrics for all models.

- **📁 trained_models/** → Trained and saved model files
  - `arma_model.pkl` → Saved ARMA model.
  - `ridge_regression.pkl` → Saved Ridge Regression model.
  - `lasso_regression.pkl` → Saved Lasso Regression model.
  - `random_forest.pkl` → Saved Random Forest model.
  - `neural_network.pkl` → Saved Neural Network model.

- **📁 reports/** → Summary reports and key findings
  - `research_report.pdf` → The full research report.
  - `insights.md` → Key insights derived from the analysis and model comparison.

## Summary of Results

Our predictions aim to help ferry operators on **Lake Constance** by forecasting water levels for the next day. 

**Key Findings:**
- The **Neural Network model** with an RMSE of **1.96** showed it could generalize patterns well.
- The **Random Forest model** was also highly effective, scoring an RMSE of **2.04**.
- **Linear regression models (Ridge, Lasso)** performed best, with a RMSE of **1.40 and 1.43**.
- The **ARMA model**, despite being a simple statistical approach, performed surprisingly well with an RMSE of **2.12**.

These findings indicate that more complex models (Neural Networks, Random Forest) capture nonlinear relationships better, while simpler models (ARMA, Linear Regression) can still yield strong results with proper feature engineering.

---
📌 *For detailed analysis, see the full research report (`reports/research_report.pdf`).*
