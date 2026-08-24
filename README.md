# Karachi-Plastic-waste-forecasting
# Karachi Plastic Waste Forecasting

Master's thesis project forecasting monthly plastic waste generation in Karachi using classical statistical, deep learning, and modern time-series models — ARIMA, LSTM, and Prophet.

## 🎯 Project Overview

Karachi generates a large and growing volume of plastic waste, and accurate forecasting is essential for municipal planning, recycling infrastructure investment, and policy design. This project builds and compares three forecasting approaches on a 60-month historical dataset (2020–2024), incorporating external regressors such as monsoon seasonality and disruption events (e.g., supply chain or civic disruptions affecting waste collection).

## 📊 Dataset

- **Time span:** 60 months (Jan 2020 – Dec 2024)
- **Split:** 48 months training / 12 months holdout
- **External regressors:** monsoon seasonality indicator, disruption-event indicator

## 🧪 Methodology

Three forecasting pipelines were built and evaluated side by side:

1. **ARIMA** — classical statistical baseline with regressor-adjusted variants
2. **LSTM** — deep learning model capturing nonlinear temporal dependencies
3. **Prophet** — decomposable trend/seasonality model, implemented with an ablation design informed by prior published work (Faisal et al.) to isolate the contribution of each component (trend, seasonality, regressors)

Each model was evaluated on the same holdout window for a fair comparison.

## 📁 Repository Structure

```
.
├── Karachi_Plastic_Waste_Forecasting_ARIMA_LSTM_Prophet_MastersThesis.ipynb   # Main analysis notebook
├── IoT_Final_Paper.pdf                                                          # Related paper/report
└── README.md
```

## 🚀 Running the Notebook

```
pip install pandas numpy statsmodels prophet tensorflow matplotlib
jupyter notebook Karachi_Plastic_Waste_Forecasting_ARIMA_LSTM_Prophet_MastersThesis.ipynb
```

## 📈 Results

*(Add: final RMSE/MAE/MAPE comparison table across ARIMA, LSTM, and Prophet on the 12-month holdout set, plus a forecast plot.)*

## ⚠️ Notes & Limitations

This project underwent a thorough internal review that flagged a few points worth being transparent about and addressing before treating results as final:

- A possible data leakage risk in the ARIMA test-set evaluation — confirm the holdout period was never used during model fitting or hyperparameter selection.
- Minor cross-chapter consistency issues in the write-up (methodology described in one section should match what's implemented in the notebook).
- One citation that could not be independently verified — worth double-checking before final submission.

## 🎓 Context

This is a Master's thesis project completed as part of a Data Science MS program (IMSciences, Peshawar).

## 📄 License

Educational/academic use.
