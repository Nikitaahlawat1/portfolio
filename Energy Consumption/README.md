# Energy Consumption 

<img width="1920" height="500" alt="image" src="https://github.com/user-attachments/assets/be1c8aa0-6f61-42e8-a508-18245fbe44ef" />

## 1. Project Overview

This project analyzes and forecasts hourly electricity demand and market prices using time-series and machine learning techniques.
Using ~35,000 hourly records of energy generation, demand, and pricing data, the project:
<ul class="tabbed-list">
  <li>Performs exploratory data analysis (EDA)</li>
  <li>Engineers time-aware and domain-specific features</li>
  <li>Benchmarks multiple forecasting approaches</li>
  <li>Compares classical statistical models with machine learning models</li>

The goal is to evaluate which modeling approach performs best for short-term electricity load forecasting.

## 2. Dataset Description

Records: 35,000+ hourly time-series entries
Features: 26 variables
Domains Covered:
  <li>Electricity generation by fuel type (fossil & renewable)</li>
  <li>Solar and wind day-ahead forecasts</li>
  <li>Total load (forecast vs actual)</li>
  <li>Market prices (day-ahead vs actual)</li>

## 3. Key Energy Sources

  <li>Fossil gas, hard coal, oil</li>
  <li>Solar, wind (onshore), biomass</li>
  <li>Hydro & pumped storage</li>

Several generation types (offshore wind, peat, shale, geothermal) were found to contain only zero or null values and were removed during data cleaning.

## 4. Exploratory Data Analysis (EDA)

Key findings:
<ul class="tabbed-list">
  <li>Strong daily (24-hour) seasonality</li>
  <li>Weekly demand cycles</li>
  <li>Electricity price moderately correlated with demand</li>
  <li>Fossil gas generation strongly correlated with price</li>
  <li>Wind generation negatively correlated with price (merit-order effect)</li>
  <li>Renewable penetration impacts price volatility</li>&nbsp;&nbsp;&nbsp;&nbsp;

Visualizations included:
<ul class="tabbed-list">
  <li>Load and price time-series</li>
  <li>Distribution analysis</li>
  <li>Correlation matrix</li>
  <li>Renewable vs fossil comparison</li>

## 5. Feature Engineering

Time-based features: hour, day, month, weekday, season
Cyclical Encoding: hour_sin, hour_cos, dow_sin, dow_cos, month_sin, month_cos
Lag features: 1h, 24h, 168h(7-day) lags
Rolling statistics: 3h, 24h, 7-day averages
Forecast residual features (forecast vs actual)
Energy Market Features: Renewable generation ratio, Demand–supply gap, Total fossil vs renewable generation

## 6. Modeling & Forecasting
### 6.1 Models Implemented

Naive Baselines: 
  <ol>Persistence (t-1)</ol>
  <ol>Seasonal Naive (t-24)</ol>&nbsp;&nbsp;&nbsp;&nbsp;
    
ARIMA / SARIMA:
  <ol>Classical statistical time-series model</ol>
  <ol>Seasonal component (24-hour cycle)</ol>
  <ol>Captures trend + autoregressive structure</ol>&nbsp;&nbsp;&nbsp;&nbsp;

XGBoost Regressor:
  <ol>Gradient boosting tree-based model</ol>
  <ol>Uses engineered features + lag variables</ol>
  <ol>Captures nonlinear relationships</ol>
  <ol>Handles interaction effects automatically</ol>

### 6.2 Evaluation Metrics
<li>MSE (Mean Squared Error)</li>
<li>MAE (Mean Absolute Error)</li>
<li>RMSE (Root Mean Squared Error</li>
<li>MAPE (Mean Absolute Percentage Error)</li>


## 7. Performance and Results
<li>Seasonal Naive performs strongly due to daily seasonality</li>
<li>SARIMA improves trend modeling</li>
<li>XGBoost generally achieves the best predictive performance</li>
