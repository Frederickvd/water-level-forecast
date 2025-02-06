# Insights & Model Comparison

## Key Insights

### Data Transformations & Feature Engineering
- **Log Transformation Improved Model Performance**  
  - Applying a **log transformation to water levels** stabilized variance and improved model accuracy, particularly for regression-based models.  

- **Deseasonalization & Detrending Were Critical for Some Models**  
  - **ARMA and Linear Regression models** required detrended and deseasonalized data for optimal performance.  
  - **Neural Networks and Random Forests** performed better with the original time-indexed data and cyclical features.
  
### Seasonality & Trend Effects
- A **strong half-yearly and yearly seasonality** was detected in water levels, confirming the need for cyclical feature engineering and deseasonalization.
- **Weather and Groundwater Features** shared clear **seasonal patterns** with water levels, while **Moon Illumination** did not exhibit shared seasonality.
- **Long-term climate trends** did not show a direct, linear effect on water levels but may contribute indirectly through changes in precipitation patterns. 

### Influence of Meteorological & Hydrological Variables
- **Water Levels Are Primarily Autoregressive**  
  - The **previous day's water level (lag-1)** was the most important predictor in all models.  
  - The Model relying solely on past water levels (ARMA) performed almost as well as those incorporating external meteorological data.  

- **Meteorological Factors Play a Secondary Role**  
  - **Precipitation** turned out to be a top feature in all models once lag-1 water level is excluded. This highlights rainfall’s short-term impact on water levels. 
  - **Snow Depth** is consistently ranked among the least important features, suggesting daily snowmelt effects are less relevant
  - **Climate Change** might drive long-term shifts in water levels (e.g., through changing temperatures), its effect on a daily timescale is limitied.

---

## Model Comparison

| Model                 | RMSE | Strengths | Weaknesses |
|-----------------------|------|------------|------------|
| **ARMA Model** | 2.12 | Simple, interpretable, good for time-dependent patterns | Ignores external features; struggles with non-stationary data |
| **Ridge Regression** | 1.40 | Handles multicollinearity, provides stable predictions | Requires extensive preprocessing to ensure linear relationships |
| **Lasso Regression** | 1.43 | Feature selection, avoids overfitting | Requires extensive preprocessing to ensure linear relationships, may zero out weak but relevant features |
| **Random Forest** | 2.04 | Captures non-linearity, interpretable feature importance | Computationally expensive; can overfit if not tuned properly |
| **Neural Network** | 1.96 | Learns complex interactions; adapts well to non-linear patterns | Requires more data, difficult to interpret |

## Conclusion & Final Takeaways
- **Short-Term Forecasting Is Primarily Driven by Autoregressive Features**  
  - The most valuable predictor was **previous water levels**, with external meteorological data adding limited predictive power.  

- **Linear Regression Models Worked Well With Proper Preprocessing**  
  - **Deseasonalization and detrending were critical** for their success.


