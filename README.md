# ⚡ Time Series Analysis — Electricity Consumption in Spain

This repository contains the R code and methodology used to model and forecast monthly electricity consumption in Spain from 1990 to 2018. The project applies time series techniques including ARIMA modeling, intervention analysis, calendar effect modeling, and outlier treatment.

## 📌 Project Context

Developed as part of the *Data Analysis* course of the **Bachelor’s Degree in Data Science and Engineering** at the **Universitat Politècnica de Catalunya (UPC)**, this project aims to build reliable models to forecast energy usage and understand influencing factors such as seasonality, holidays, and economic changes.

## 📊 Dataset

- **Source:** Spanish Ministry of Industry, Commerce and Tourism  
- **Metric:** Monthly gross domestic electricity consumption (in GWh)  
- **Time Period:** January 1990 – December 2018  
- **Observations:** 347

## 🧠 Methodology

The project follows the **Box-Jenkins methodology**:
1. **Transformation & Stationarity:** Log-transform and seasonal differencing to stabilize variance and remove seasonality.
2. **Model Identification:** Use of ACF/PACF plots to propose ARIMA models.
3. **Estimation & Validation:** Fit models and analyze residuals for assumptions (independence, normality, homoscedasticity).
4. **Forecasting:** Evaluate model performance using RMSE, MAE, MAPE.
5. **Enhancements:**  
   - Add **calendar effects** (Easter, Trading Days).  
   - Apply **intervention analysis** for known historical events.  
   - Perform **outlier detection and treatment**.

## 🔍 Models Evaluated

- `mod1`: ARIMA(0,1,2)(0,1,1)[12]
- `modEC`: Includes calendar effects (Easter + trading days)
- `modEClin`: Includes calendar effects and outlier treatment → best model for fit

## 📈 Key Results

- Final model: **ARIMA(0,1,4)(0,1,1)[12]** with calendar and outlier adjustments.
- Produces accurate forecasts with improved AIC/BIC.
- Captures seasonal patterns and reduces forecasting error.

## 🛠️ Tools & Libraries

- R 4.x
- `forecast`
- `tseries`
- `ggplot2`
- Other time series analysis libraries
