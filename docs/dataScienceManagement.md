# dataScienceManagement
-----------------------
This is for management if your data by forecasting an anomaly detection

## Functionality
* [Isolation Forest Anomaly Detection](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataScienceManagement.md#isolation-forest-anomaly-detection)
* [Auto Sarima Daily Forecast](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataScienceManagement.md#auto-sarima-daily-forecast)
* [Prophet Forecast](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataScienceManagement.md#prophet-forecast)


## Dependencies
* pandas
* matplotlib
* scikit learn
* pmdarima
* prophet

## Common Input Parameters
* dateColumn - This is the string value column name for your date column in your dataset
* valueColumn - This is the string value column name for your value column in your dataset
* df - This dataframe will contain your two needed columns of dateColumn and valueColumn

## Isolation Forest Anomaly Detection
```python
isolationForestAnomalyDetection(dataset=pandasDataFrame, dateColumn=str, valueColumn=str, contamination=int)
```
* contamination - Use this to set the expected amount of outliers present in your dataset
## Auto SARIMA Daily Forecast
```python
autoSARIMADailyForecast(df=pandasDataFrame, dateColumn=str, valueColumn=str, predStartDate=str, predEndDate=str, predPeriods=int, lookBackDate=str)
```
* predStartDate - Use this to set the start of your prediction
* predEndDate - Use this to set the end of your prediction
* predPeriod - Use this to set how many periods you are predicting for. WARNING: The difference between predStartDate and predEndDate must match your periods
* lookBackDate - Use this to set the amount of dates that will show in the visualization of your forecast
## Prophet Forecast
```python
prophetForecast(df=pandasDataFrame, dateColumn=str, valueColumn=str, numPeriods=int, freqType=str)
```
* freqType will be for the type of time value, day, month, year, etc

