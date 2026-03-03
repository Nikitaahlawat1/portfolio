# Energy Consumption 

<img width="1920" height="500" alt="image" src="https://github.com/user-attachments/assets/be1c8aa0-6f61-42e8-a508-18245fbe44ef" />

## 1. Project Overview

This project analyzes and forecasts hourly electricity demand and market prices using time-series and machine learning techniques.

Using ~35,000 hourly records of energy generation, demand, and pricing data, the project:

<li>Performs exploratory data analysis (EDA)<\li>

Engineers time-aware and domain-specific features

Benchmarks multiple forecasting approaches

Compares classical statistical models with machine learning models

The goal is to evaluate which modeling approach performs best for short-term electricity load forecasting.

## 2. Dataset Description

Records: 35,000+ hourly time-series entries
Features: 26 variables
Domains Covered:

  Electricity generation by fuel type (fossil & renewable)
  Solar and wind day-ahead forecasts
  Total load (forecast vs actual)
  Market prices (day-ahead vs actual)

## 3. Key Energy Sources

  Fossil gas, hard coal, oil
  Solar, wind (onshore), biomass
  Hydro & pumped storage

Several generation types (offshore wind, peat, shale, geothermal) were found to contain only zero or null values and were removed during data cleaning.

## 4. Data Cleaning & Preprocessing

Handled missing values (<0.1%) using time-series interpolation
Removed 100% null or zero-information columns
Standardized timestamps and ensured hourly continuity
Created aggregate features:
  Renewable generation total
  Fossil generation total
  Net pumped storage contribution

## 5. Exploratory Data Analysis (EDA)

Energy mix composition and contribution analysis
Seasonal and diurnal patterns in load and renewables
Correlation analysis between:
  Renewables and prices
  Load and fossil generation
Distribution analysis of electricity prices

### 5.1 Key Insight:
High renewable penetration (solar & wind) is associated with increased short-term price volatility, increasing the importance of accurate forecasting.

## 6. Feature Engineering

Time-based features: hour, day, month, weekday, season
Lag features: 1h, 24h, 7-day lags
Rolling statistics: 3h, 24h, 7-day averages
Forecast residual features (forecast vs actual)

## 7. Modeling & Forecasting
### 7.1 Models Implemented
Baseline statistical models
Machine Learning:
  Linear Regression
  Random Forest
  XGBoost

Time-Series Models:
  LSTM (optional extension)

### 7.2 Evaluation Metrics
MAE (Mean Absolute Error)
RMSE (Root Mean Squared Error)

## 8. Performance

Achieved ~15–25% improvement in RMSE over baseline models
Strong alignment between forecasted and actual load values
Robust renewable generation forecasting performance
