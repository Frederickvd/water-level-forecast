# Predicting Water Levels of Lake Constance

This repository contains a project developed for the *Workshop Fundamentals of Data Science* course, focusing on **water level forecasting at Lake Constance**. The project applies machine learning and time series modeling techniques to predict next-day water levels based on meteorological, hydrological, and climate change data.


- [Predicting Water Levels of Lake Constance](#predicting-water-levels-of-lake-constance)
- [Contributors](#contributors)
- [Setup](#setup)
  - [Installation](#installation)
  - [Data](#data)
  - [Model Weights](#model-weights)
  - [Results](#results)
- [Source Code Directory Tree](#source-code-directory-tree)

## Contributors

- Frederick von Dobbeler
- Ines Goutenmacher
- Ruben Cardell
- Sina Schlegel

## Setup
### Installation
To set up a local development environment, follow these steps:

1. Clone the repository:
```bash
   git clone https://github.com/Sinus4096/water-level-forecast.git
````
2. Navigate to the cloned repository:
```bash
cd water-level-forecast
```
3. To replicate our results we suggest setting up a conda environment (or any other virtual environment) and then installing the required packages:

```bash
conda create -n water_level_forecast python=3.10 pip
conda activate water_level_forecast
pip install -r requirements.txt
```

### Data
All datasets are stored in the `data` directory and are divided into raw and processed datasets.

### Model Weights

The trained models are stored in `results/trained_models/`:

- `ridge_regression.pkl` – Trained Ridge Regression model  
- `lasso_regression.pkl` – Trained Lasso Regression model  
- `random_forest.pkl` – Trained Random Forest model  
- `arma_model.pkl` – Trained ARMA model  
- `neural_network.pkl` – Trained Neural Network model  

### Results
All visualizations, error metrics, and model performance reports are saved in the `results/` directory.


## Source Code Directory Tree
```bash
.
├── data                                # Raw and processed datasets
│   ├── raw/                                # Unprocessed datasets
│   └── processed/                          # Preprocessed datasets
├── notebooks                            # Jupyter Notebooks for data processing, training, and evaluation
├── results                              # Model outputs, visualizations, and reports
│   ├── trained_models/                      # Saved model files
│   ├── plots/                               # Graphs and visualizations
│   ├── metrics/                             # Evaluation metrics
│   ├── reports/                             # Summary reports
└── README.md                            # Project documentation
```
