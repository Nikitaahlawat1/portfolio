# Energy Consumption 

![images](https://github.com/user-attachments/assets/be1c8aa0-6f61-42e8-a508-18245fbe44ef)


## Project Overview

This project delivers an end-to-end data science analysis and forecasting pipeline for electricity generation, system load, and market prices using 35,000+ hourly observations.
The goal is to understand energy mix dynamics, renewable variability, and market behaviour, and to build accurate forecasting models to support energy planning and decision-making.

### Dataset Description

Records: 35,000+ hourly time-series entries
Features: 26 variables
Domains Covered:

  Electricity generation by fuel type (fossil & renewable)
  Solar and wind day-ahead forecasts
  Total load (forecast vs actual)
  Market prices (day-ahead vs actual)

### Key Energy Sources

  Fossil gas, hard coal, oil
  Solar, wind (onshore), biomass
  Hydro & pumped storage

Several generation types (offshore wind, peat, shale, geothermal) were found to contain only zero or null values and were removed during data cleaning.

### Data Cleaning & Preprocessing

Handled missing values (<0.1%) using time-series interpolation
Removed 100% null or zero-information columns
Standardized timestamps and ensured hourly continuity
Created aggregate features:
  Renewable generation total
  Fossil generation total
  Net pumped storage contribution

### Exploratory Data Analysis (EDA)

Energy mix composition and contribution analysis
Seasonal and diurnal patterns in load and renewables
Correlation analysis between:
  Renewables and prices
  Load and fossil generation
Distribution analysis of electricity prices

#### Key Insight:
High renewable penetration (solar & wind) is associated with increased short-term price volatility, increasing the importance of accurate forecasting.

### Feature Engineering

Time-based features: hour, day, month, weekday, season
Lag features: 1h, 24h, 7-day lags
Rolling statistics: 3h, 24h, 7-day averages
Forecast residual features (forecast vs actual)

### Modeling & Forecasting
#### Models Implemented
Baseline statistical models
Machine Learning:
  Linear Regression
  Random Forest
  XGBoost

Time-Series Models:
  LSTM (optional extension)

#### Evaluation Metrics
MAE (Mean Absolute Error)
RMSE (Root Mean Squared Error)

### Performance

Achieved ~15–25% improvement in RMSE over baseline models
Strong alignment between forecasted and actual load values
Robust renewable generation forecasting performance
