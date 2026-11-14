# Predictive Analytics Using Historical Data

Forecasting monthly sales from four years of historical data (2015-2018) using regression and time-series models.

## What It Does
- Cleans the data and builds a **48-month sales time series**
- Creates trend and month-of-year features
- Trains two models on the first 42 months and tests them on the last 6 months:
  - **Linear Regression** (trend + seasonality features)
  - **Holt-Winters Exponential Smoothing**
- Evaluates accuracy with MAE, RMSE and MAPE
- Forecasts the next 6 months with the better model

## Results
| Model | MAE | RMSE | MAPE |
|---|---|---|---|
| Linear Regression | 14,681 | 18,498 | 17.7% |
| Holt-Winters | 13,134 | 18,420 | 15.8% |

**Holt-Winters performed slightly better** and was used for the final forecast. Both models follow the overall pattern but underestimate sharp sales peaks, such as November 2018.

## 6-Month Forecast (Holt-Winters)
| Month | Forecast Sales |
|---|---|
| Jan 2019 | $49,393 |
| Feb 2019 | $41,600 |
| Mar 2019 | $71,943 |
| Apr 2019 | $60,876 |
| May 2019 | $68,134 |
| Jun 2019 | $62,708 |

## Limitations
Only 4 years of data, a small 6-month test set, and no outside factors such as promotions or pricing.

## How to Run
1. Open `Predictive_Analytics_Historical_Data.ipynb` in Google Colab
2. Upload `train.csv` to the Files panel
3. Click Runtime -> Run all

## Dataset
[Superstore Sales (Kaggle)](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting)

## Tools
Python, Pandas, NumPy, scikit-learn, statsmodels, Plotly

## Author
Abhinav Gaur
