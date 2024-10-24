# reportingManagement
-----------------------
This module is used of the CJA Reporting API and provides significant value for extracting data

## Functionality
* [Get Single Call Report](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/reportingManagement.md#get-single-call-report)
* [Get Total Table Rows](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/reportingManagement.md#get-total-table-rows)
* [Get Total Table Pages](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/reportingManagement.md#get-total-table-pages)
* [Get All Rows Report](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/reportingManagement.md#get-all-rows-report)
* [Monthly Time Series Report](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/reportingManagement.md#monthly-time-series-report)
* [Daily Time Series Report](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/reportingManagement.md#daily-time-series-report)
* [Five Metrics Report](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/reportingManagement.md#five-metrics-report)
* [Breakdown Report](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/reportingManagement.md#breakdown-report)


## Dependencies
* pandas
* requests
* json
* time
* numpy


## Common Input Parameters
* headers are generated using the auth file and are required for all calls
* reqNum is an optional parameter that can be used to set the number of rertries
* dataViewId is the unique identifier of the dataView
* startDate this is formatted in the standard `YYYY-MM-DD` format
* endDate this is formatted in the standard `YYYY-MM-DD` format
* metric this is the schema location for a single emtric
* metrics this is a list of metrics, it must contain five separate entries in list format
* rowsPerPage allows you to set the number of rows per page of pull, can accept a max of int0000
* limit this is differentiated as an input name, but is functionally the same as rowsPerPage

## Get Single Call Report
```python
getSingleCallReport(headers=dict, body=dict, reqNum=int)
```

## Get Total Table Rows
```python
getTotalTableRows(headers=dict, body=dict, reqNum=int)
```

## Get Total Table Pages
```python
getTotalTablePages(headers=dict, body=dict, reqNum=int)
```

## Get All Rows Report
```python
getAllRowsReport(headers=dict, body=dict, rowsPerPage=int, reqNum=int)
```

## Monthly Time Series Report
```python
monthlyTimeSeriesReport(headers=dict, dataViewId=str, startDate=str, endDate=str, metric=str, reqNum=int, limit=int0000)
```
* This will get a month based report for a single metric

## Daily Time Series Report
```python
dailyTimeSeriesReport(headers=dict, dataViewId=str, startDate=str, endDate=str, metric=str, reqNum=int, limit=int0000)
```
* This will get a day's based report for a single metric

## Five Metrics Report
```python
fiveMetricReport(headers=dict, dataViewId=str, startDate=str, endDate=str, metrics=list, dimension=str, rowsPerPage=int, reqNum=int, limit=int0000)
```
* You must include five metrics in the entry for this to work and in a list format

## Breakdown Report
```python
breakdownReport(headers=dict, dataViewId=str, startDate=str, endDate=str, dimension=str, metric=str, rowsPerPage=int, breakdownDim=str, reqNum=int, limit=int0000)
```
* This will breakdown a single metric by two dimensions, rowsPerPage will set the rows per page for each dimension


