# AAI-500 Final Project — Team 3
## Modeling Household Energy Waste and Efficiency Using Smart-Home Sensor Data

### Team Members
- Ashley Figueroa
- Robert Shifrin
- Carlo Casella

### Project Overview
This project develops predictive models for household appliance energy consumption in a low-energy “passive” home in Belgium. We analyze how environmental sensor data (temperature, humidity), weather variables, and temporal features relate to appliance energy usage, and we evaluate multiple regression models to identify patterns associated with inefficient (higher-than-expected) consumption.

### Dataset
- **Source:** UCI Machine Learning Repository — Appliances Energy Prediction
- **Size:** 19,735 observations (10-minute intervals over ~4.5 months)
- **Target:** `Appliances` (Wh)

### Methods
1. Data cleaning and feature engineering (datetime parsing, hour, NSM, weekend indicators)
2. Exploratory Data Analysis (distributions, time-of-day patterns, correlations)
3. Model comparison:
   - Linear Regression (baseline)
   - Ridge Regression (regularization / multicollinearity)
   - Random Forest Regression (nonlinear interactions)

### Evaluation Metrics
MAE, RMSE, R² on an 80/20 train/test split.

### Operational Definition: Waste vs Efficiency
We define *relative energy waste* using model residuals:
- **Waste:** Observed consumption > Predicted baseline (positive residual)
- **Efficiency:** Observed consumption < Predicted baseline (negative residual)

### How to Run
Open the notebook and run cells top-to-bottom. For reproducibility, load the dataset directly from the UCI URL inside the notebook (no manual download required).

### Requirements
Python 3.x with: numpy, pandas, matplotlib, seaborn, scikit-learn
