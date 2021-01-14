# Sales-forecasting-with-Prophet-and-Time-series
Use Facebook Prophet model to forecast Sales including seasonality patterns

In this notebook, Prophet model is used to forecast Sales at store level with high seasonality effects.

# Dataset
The dataset used collects daily historical sales data from 1,115 Rossmann stores over 31 months resulting into 1+ million transaction records. In addition to transactions, the dataset includes information about promotions, competition and holiday periods at store level. This info is used to incorporate holidays during forecasting step.
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
- Prophet performs very well when seasonality is high. The model's perfromance is evaluated using RMSE metric. It shows that the error remains constant over the projected horizon.

![](asset/performance.jpg) 

# Results

Forecast over 90 days example:
![](asset/newplot.png)

The additive model analyzes variations at multiple levels:
- long-term base trend
- seasonal 'noise' (yearly, monthly, weekly and daily)
- impact from holidays. In the last picture below, we see some sales spikes explained by holidays. These are then integrated into the forecasting model.

![](asset/trend.jpg)

![](asset/seasonality.jpg)

![](asset/holidays.jpg)


# Dependencies
- Facebook Prophet (pip install fbprophet)

# Next
- benchmark prediction performance against other models :
  - LSTM network
  - XGBoost
  - StatModels
  - Others
