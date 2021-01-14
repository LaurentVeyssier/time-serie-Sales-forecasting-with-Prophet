# Sales-forecasting-with-Prophet-and-Time-series
Use Facebook Prophet model to forecast Sales including seasonality patterns

In this notebook, Prophet model is used to forecast Sales at store level with high seasonality effects.

# Dataset
The dataset used collects daily sales from over 1000 stores and 31 months resulting into over 1 million transaction logs. In addition to transactions, the dataset includes information about promotions and holiday periods at store level. This is used to incorporate holiday information during forecasting step.
The dataset is available on kaggle [here](https://www.kaggle.com/c/rossmann-store-sales/data).

# Project structure
1) Exploration and cleaning of the data.
  - Sales reveal a high seasonality at multiple timescale: during the year, within a month and also during a typical week. The seasonality is illustrated below.

![](asset/monthly.jpg)

![](asset/daily.jpg)

  - The analysis also indicates a positive impact from promotions on sales and customer frequentation.
  
 ![](asset/promo.jpg) 

2) Forecasting using Prophet
  - without information on holidays
  - including detailed information on holiday periods
  
3) Performance evaluation


# Results

Forecast over 90 days example:
![](asset/newplot.png)

The additive model analyzes variations are multiple levels:
- long-term trend
- seasonal trends (yearly, monthly, weekly and daily)
- impact from holidays. In this last graph below, we see some spikes explained by holidays which are then integrated into the forecasting model.

![](asset/trend.jpg)

![](asset/seasonality.jpg)

![](asset/holidays.jpg)


# Dependencies
- Facebook Prophet (pip install fbprophet)
