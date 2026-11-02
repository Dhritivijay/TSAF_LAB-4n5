# Time Series Forecasting – ARIMA and SARIMA

This repository contains the implementation of **Lab Exercise 4 and Lab Exercise 5** for Time Series Analysis and Forecasting. The experiments demonstrate time-series modelling, stationarity analysis, differencing, forecasting, and model evaluation using ARIMA and Seasonal ARIMA (SARIMA).

## 📌 Experiments

### Experiment 4: ARIMA Model Implementation and Forecasting

**Aim:** To implement an ARIMA model on a real-world time-series dataset, generate forecasts, and evaluate prediction accuracy.

- Dataset: AirPassengers (monthly international airline passenger counts)
- Model: `ARIMA(2, 1, 2)`
- Train-test split: 80% training and 20% testing
- Stationarity analysis using the Augmented Dickey-Fuller (ADF) test
- First-order differencing
- ACF and PACF analysis
- Forecasting and residual analysis

**Evaluation metrics:**

| Metric | Result |
|---|---:|
| MAE | 63.545 |
| RMSE | 82.513 |

### Experiment 5: Seasonal ARIMA (SARIMA) Forecasting

**Aim:** To implement a Seasonal ARIMA model on a seasonal time-series dataset and evaluate its forecasting performance.

- Dataset: AirPassengers
- Model: `SARIMA(1,1,1)(1,1,1,12)`
- Seasonal period: 12 months
- Train-test split: 80% training and 20% testing
- Seasonal differencing
- Seasonal ACF and PACF analysis
- Forecasting and residual analysis

**Evaluation metrics:**

| Metric | Result |
|---|---:|
| MAE | 25.268 |
| RMSE | 31.787 |

## 🧠 Concepts Covered

- Time-series data and its components
- Stationarity and the Augmented Dickey-Fuller test
- First-order and seasonal differencing
- Autocorrelation Function (ACF)
- Partial Autocorrelation Function (PACF)
- ARIMA parameters: p, d, q
- SARIMA parameters: p, d, q, P, D, Q, s
- Chronological train-test splitting
- Forecasting and residual analysis
- Model evaluation using MAE and RMSE

## ⚙️ Technologies and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Scikit-learn

## 📂 Project Structure

```text
Time-Series-Forecasting/
│
├── ARIMA/
│   ├── arima_implementation.py
│   └── plots/
│
├── SARIMA/
│   ├── sarima_implementation.py
│   └── plots/
│
├── README.md
└── requirements.txt
```

*The structure above is a suggested organization. Adjust the filenames and folders to match the files in your repository.*

## 🚀 Installation and Execution

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd Time-Series-Forecasting
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

Or install the packages directly:

```bash
pip install pandas numpy matplotlib statsmodels scikit-learn
```

### 3. Run the experiments

For ARIMA:

```bash
python ARIMA/arima_implementation.py
```

For SARIMA:

```bash
python SARIMA/sarima_implementation.py
```

The dataset is loaded from the following source:

`https://raw.githubusercontent.com/jbrownlee/Datasets/master/airline-passengers.csv`

An active internet connection is required to download the dataset when running the code.

## 📊 ARIMA vs SARIMA

| Comparison | ARIMA | SARIMA |
|---|---|---|
| Seasonal modelling | Not explicitly modelled | Explicitly modelled |
| Parameters | p, d, q | p, d, q, P, D, Q, s |
| MAE | 63.545 | 25.268 |
| RMSE | 82.513 | 31.787 |

In the main experiment, SARIMA achieved lower MAE and RMSE than ARIMA. This indicates that explicitly modelling the annual seasonal pattern improved forecasting performance on the selected test period.

## 🔬 Independent Tasks

The practical exercises also include:

- Comparing different ARIMA orders.
- Studying the effect of differencing.
- Comparing different forecast horizons.
- Performing residual analysis.
- Applying ARIMA to another real-world dataset.
- Comparing multiple SARIMA configurations.
- Studying different seasonal periods.
- Comparing ARIMA and SARIMA forecasts.
- Investigating seasonal differencing.
- Applying SARIMA to monthly Mauna Loa CO₂ measurements.

## 🎯 Conclusion

These experiments demonstrate how ARIMA and SARIMA can be used for time-series forecasting. ARIMA models non-seasonal time-series behaviour, while SARIMA extends the approach by incorporating seasonal components. The results highlight the importance of stationarity, differencing, seasonal patterns, model selection, and forecast evaluation when building reliable time-series models.

---

**Course:** Time Series Analysis and Forecasting  
**Lab Exercises:** 4 and 5  
**Language:** Python
