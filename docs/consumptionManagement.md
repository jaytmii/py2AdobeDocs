# consumptionManagement
-----------------------
This area of functions is for tracking your CJA consumption. Due to processing timelines Adobe doesnt update until the 4th for prior month's data

## Functionality
* [Get Cumulative Reportable Rows](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/consumptionManagement.md#get-cumulative-reportable-rows)
* [Get Monthly Reportable Rows](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/consumptionManagement.md#get-monthly-reportable-rows)
* [Get Yearly Reportable Rows](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/consumptionManagement.md#get-yearly-reportable-rows)


## Dependencies
* pandas
* requests
* json
* time
* numpy
* datetime

## Common Input Parameters
* headers are generated using the auth file and are required for all calls
* reqNum is an optional parameter that can be used to set the number of rertries
* startMonth this is in a string format and capitalized, as in `APRIL`, `MAY`
* endMonth this is in a string format and capitalized
* startYear this is in a string format
* endYear this is in a string format

## Get Cumulative Reportable Rows
```python
getCumulativeReportableRows(headers=dict, startMonth=str, startYear=str, endMonth=str, endYear=str, reqNum=5)
```

## Get Monthly Reportable Rows
```python
getMonthlyReportableRows(headers=dict, startMonth=str, startYear=str, endMonth=str, endYear=str, reqNum=5)
```


## Get Yearly Reportable Rows
```python
getYearlyReportableRows(headers=dict, startMonth=str, startYear=str, endMonth=str, endYear=str, reqNum=5)
```



