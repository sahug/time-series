# Time Series Analysis

While building a model for time series analysis during the model training we take some amount of past data, called lag or window, based on time range, it coluld be last 1 hour, last 1 day or last 1 year, etc. These range of data will be our inputs. The output will be the corresponding prediction, next hour, next day or next year based on the dataset or problem in hand.

**Example:**

Lets say we have a dataset that records temperature per day, 60 records in total, and we want to predict the temperature next day. 

Here we will select lag or window, ex: 7 days. 6 days will be input and 7th day will be output. 

The same logic can be applied to any time series dataset once we know the time range, hour, day, year on which the record is available and what time range we are predicting.

**ARMA (Auto Regressive Moving Average)**

If we are using ARMA we provide some values, coefficients for AR and MA. These coefficents are nothing but lags. The model then makes this split and predicts the next value and compares it with the actual value. These coefficient can be different for AR and MA and it depends how far back we want to look for calculating each AR and MA.

**ARIMA (Auto Regressive Integrated Moving Average)**

Similar to ARMA here also we provide some lags to calculate AR and MA. Alomg with this we also provide value for I i.e. number of differencing required to make the time series stationary. 

**Other Models**

In some cases depending on model we need to provide the feature, X, and labels, y, seperatly. We can create these X and Y by using this same logic. For the example above we will take the first 6 records and save it as X and the 7th records as Y. Basically create a matrix where 1 - 6 days are each individual features and 7th day is a output, y.

## Table
|Project|Description|
|-------|-----------|
|TSA - Basics - Simple, Cumulative, Exponential, ACF, PACF, ARM, MA, ARIMA|Simple, Cumulative, Exponential, ACF, PACF, ARM, MA, ARIMA|
|TSA - Basics - Introduction to Date and Time|Timestamp, Periods, DateRange, ToDateTime, Shifting, Lags, Resampling|
|TSA - Basics - Finance and Statistics|PercentChange, StockReturn, AbsChange, CompareTimeSeries, WindowFunction, OHLCChart, CandlestickChart, ACF, PACF|
|TSA - Basics - Decomposition and Random Walks|Trends, Seasonality, Noise, WhiteNoise, RandomWalk, Stationarity|
|TSA - Basics - Modeling using StatsModels|AR, MA, ARMA, ARIMA, VAR, SARIMA|
