# Virginia Housing Price Prediction with XGBoost

This project predicts median home sales prices across Virginia counties and cities using a custom dataset I created. The dataset integrates 17 key features from multiple publicly available sources, including:

- **Home Sales by County/City** (Monthly, 2016–present)  
- **Median Sales Prices by County/City** (Monthly, 2016–present)  
- **Residential Building Permits by County/City** (Annual, 2000–present)  
- **Mortgage Rates** (Weekly, 2016–present)  
- **U.S. Gross Domestic Product** (Quarterly, 2009–present)  
- **Job Totals, U.S. and Virginia** (Monthly, 2009–present)  
- **Unemployment Rate, U.S. and Virginia** (Monthly, 2009–present)  
- **County and City Population Totals** (2010–2023)  

The dataset was carefully merged and cleaned to include these 17 features, capturing a broad range of economic, demographic, and housing market factors influencing home prices.

---

## Modeling Approach

- Split data into training and testing sets (80/20 split)
- Log-transformed the target variable (`median_sales_price`) for stability
- Trained an **XGBoost Regressor** with tuned hyperparameters:
  - `n_estimators=320`
  - `learning_rate=0.11`
  - `min_child_weight=2`
- Used cross-validation for model selection and evaluation

---

## Results

After tuning, the model achieved:

- **R² Score**: ~0.81  
- **RMSE**: ~$53,700  
- **MAE**: ~33,200  

Visualizations include:

- Scatter plot: Actual vs Predicted Prices  
- Histogram: Residual Error Distribution

---

## Project Contents

This repository includes:

- Data preprocessing and feature engineering
- XGBoost model training and hyperparameter tuning
- Evaluation metrics and result plots

---

## Data Source

All data sourced from [Virginia Realtors Research](https://virginiarealtors.org/research/data/).

---
