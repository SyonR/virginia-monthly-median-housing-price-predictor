# virginia-monthly-median-housing-price-predictor
Virginia Housing Price Prediction Using XGBoost
This project predicts median home sales prices across Virginia counties using a custom dataset I created by combining and cleaning multiple datasets from the Virginia Realtors Research Data portal.

Dataset and Features
Integrated features include housing permits, home sales volume, population, GDP figures, and multiple mortgage interest rates.

Data cleaning included dropping rows with missing critical feature or target values and applying log transformation to the target variable for improved model stability.

Modeling Approach
Split data into train/test sets (80/20).

Trained an XGBoost regression model with tuned hyperparameters (n_estimators=320, learning_rate=0.11, min_child_weight=2).

Hyperparameter tuning boosted model R² from ~0.79 to ~0.81 and reduced RMSE from ~$56,600 to ~$53,700.

Evaluation
Evaluated model performance using MAE, RMSE, and R² metrics.

Visualized predictions vs. actual prices and residual error distributions for deeper insight.
