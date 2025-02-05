# Results

This folder contains the results from our model predictions and evaluations for forecasting water levels in **Lake Constance**.

## 📂 Contents:

- **📁 plots/** → Key visualizations generated during the analysis
  - `water_levels_pred_vs_actual.png` → Comparison of predicted vs actual water levels.
  - `feature_importance_rf.png` → Feature importance ranking from the Random Forest model.
  - `feature_importance_nn.png` → Feature importance ranking from the Neural Network model.
  - `arma_forecast.png` → ARMA model's rolling forecast for water levels.
  - `ridge_vs_lasso_residuals.png` → Residuals distribution for Ridge vs. Lasso Regression.
  - `rmse_comparison.png` → RMSE comparison for all models.
  - `seasonality_analysis.png` → Detected seasonality trends in water levels.

- **📁 metrics/** → Evaluation metrics for model performance
  - `model_performance.csv` → RMSE, MSE, and other evaluation metrics for all models.
  - `residuals_analysis.csv` → Table of residuals (errors) for each prediction.

- **📁 trained_models/** → Trained and saved model files
  - `arma_model.pkl` → Saved ARMA model.
  - `ridge_regression.pkl` → Saved Ridge Regression model.
  - `lasso_regression.pkl` → Saved Lasso Regression model.
  - `random_forest.pkl` → Saved Random Forest model.
  - `neural_network.pkl` → Saved Neural Network model.

- **📁 reports/** → Summary reports and key findings
  - `model_comparison.md` → A discussion on the strengths and weaknesses of each model.
  - `research_report.pdf` → The full research report.
  - `insights.md` → Key insights derived from the analysis.

## Summary of Results

Our predictions aim to help ferry operators on **Lake Constance** by forecasting water levels for the next day. 

**Key Findings:**
- The **Neural Network model** performed best, with an RMSE of **1.96**, showing it could generalize patterns well.
- The **Random Forest model** was also highly effective, scoring an RMSE of **2.04**.
- **Linear regression models (Ridge, Lasso)** had a lower RMSE of **1.40 and 1.43**, making them interpretable but slightly less accurate.
- The **ARMA model**, despite being a simple statistical approach, performed surprisingly well with an RMSE of **2.12**.

These findings indicate that more complex models (Neural Networks, Random Forest) capture nonlinear relationships better, while simpler models (ARMA, Linear Regression) can still yield strong results with proper feature engineering.

---
📌 *For detailed analysis, see the full research report (`reports/research_report.pdf`).*
