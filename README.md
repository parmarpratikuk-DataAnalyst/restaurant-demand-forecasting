# Restaurant Demand Forecasting
### A Hybrid SARIMAX and Random Forest Framework

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## Overview

This project develops and compares three demand forecasting models for 
restaurant operations using a real-world dataset of 50 restaurants over 
12 months (Jan 2024 – Jan 2025, ~10,000 records).

The goal was to predict daily quantity sold per restaurant by combining 
time-series modelling with machine learning, incorporating exogenous 
variables such as weather, promotions and special events.

**Best model: Random Forest — R² 0.76, RMSE 109.03, MAE 80.11**

---

## Models Compared

| Model | RMSE | MAE | R² |
|-------|------|-----|----|
| Random Forest | 109.03 | 80.11 | 0.76 |
| Hybrid (Stacked) | 2653.04 | 2075.43 | 0.34 |
| SARIMAX | 3052.63 | 2140.50 | 0.13 |

---

## Key Findings

- **Random Forest** outperformed all models, capturing non-linear 
  relationships between pricing, promotions and temporal patterns
- **Price difference** (actual vs market price) was the strongest 
  demand predictor
- **Promotions and special events** caused measurable demand spikes 
  that traditional time-series models could not capture
- **SARIMAX** captured trends and seasonality but failed on 
  non-linear demand patterns
- **Hybrid model** showed that combining models requires careful 
  data alignment — a key methodological finding

---

## Tech Stack

- **Python** — Pandas, NumPy, Scikit-learn, Statsmodels
- **ML Models** — Random Forest Regressor, SARIMAX, Linear Regression (meta-learner)
- **Visualisation** — Matplotlib, Seaborn
- **Feature Engineering** — Lag features, rolling statistics, 
  time-based features, price ratios

---

## Project Structure

    restaurant-demand-forecasting/
    │
    ├── notebooks/
    │   └── demand_forecasting.ipynb
    ├── data/
    │   └── README.md
    ├── requirements.txt
    └── README.md


## How to Run

```bash
git clone https://github.com/parmarpratikuk-DataAnalyst/restaurant-demand-forecasting.git
cd restaurant-demand-forecasting
pip install -r requirements.txt
jupyter notebook notebooks/demand_forecasting.ipynb
```

---

## Author

**Pratik R Parmar**  
MSc Data Analytics — London Metropolitan University (2025)  
[LinkedIn](https://www.linkedin.com/in/pratik1510)

---

*MSc Dissertation Project — submitted May 2026*
