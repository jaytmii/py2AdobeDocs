# calculatedMetricsManagement
-----------------------
There is significant functionality provided by the official API endpoints and this wrapper:

## Functionality
* [Get Calculated Metric Use Report](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#get-calculated-metric-use-report)
* [Get Calculated Metric Definition](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#get-calculated-metric-definition)
* [Get Calculated Metric Compatibility](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#get-calculatedmetric-compatibility)
* [Get Calculated Metric Owner](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#get-calculated-metric-owner)
* [Get Calculated Metric](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#get-caclculated-metric)
* [Copy Calculated Metric](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#copy-calculated-metric)
* [Get Total Calculated Metrics Count](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#copy-calculated-metric)
* [Share Calculated Metric To All](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#share-calculated-metric-to-all)
* [Unshare Calculated Metric To All](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#unshare-calculated-metric-to-all-users)
* [Share Calculated Metric To User](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#share-calculated-metric-to-user)
* [Share Calculated Metric To Group](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#share-calculated-metric-to-group)
* [Get Company Calculated Metrics](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#get-company-calculated-metrics)
* [Update Calculated Metric](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#update-calculated-metric)
* [Approve Calculated Metric](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#approve-calculated-metric)
* [Disapprove Calculated Metric](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#disapprove-calculated-metric)
* [Delete A Calculated Metric](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#delete-calculated-metric)
* [Calculated Metric Usage](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md#calculated-metric-usage)


## Dependencies
* pandas
* requests
* json
* time
* numpy

## Common Input Parameters
* headers are generated using the auth file and are required for all calls
* reqNum is an optional parameter that can be used to set the number of rertries
* metricId is an alpha numeric string unique identifier for metrics, it can be found in the URL
* definition contains the json formatted logic of the metric
* dataViewId is the unique Id of the dataView

## Get Calculated Metric Use Report
```python
getCalculatedMetricUseReport(headers=dict, metricId=str, reqNum = 5)
```

## Get Calculated Metric Definition
```python
getCalculatedMetricDefinition(headers=dict, metricId=str, reqNum = 5)
```
* Contains all the logic powering the calculation

## Get CalculatedMetric Compatibility
```python
getCalculatedMetricCompatibility(headers=dict, metricId=str, reqNum = 5)
```
* For pulling information on the functions, the metrics used in the calculation, and their path

## Get Calculated Metric Owner
```python
getCalculatedMetricOwner(headers=dict, dmetricId = str, reqNum = 5)
```

## Get Caclculated Metric
```python
getCalculatedMetric(headers=dict, metricId=str, reqNum=5)
```

## Copy Calculated Metric
```python
copyCalculatedMetric(headers=dict, owner=str, metricId=str,dataViewId=str,cmName=str,cmDescription=str,reqNum=5)
```
* cmName is for the new calculated metrics name. If not included "(Copy)" will be appended to the end of the original name
* cmDescription is the new metric's description, otherwise it will pull in the original metrics description


## Get Total Calculated Metrics Count
```python
getTotalCalculatedMetricsCount(headers=dict, reqNum=5)
```
* This is used to get the total count of calculatedMetrics in the instance

## Share Calculated Metric To All
```python
shareCalculatedMetricToAll(headers=dict, metricId=str, reqNum=5)
```
* Share to all Users

## Unshare Calculated Metric To All Users
```python
unshareCalculatedMetricToAll(headers=dict, metricId=str, reqNum=5)
```
* Remove share to all users

## Share Calculated Metric To User
```python
shareCalculatedMetricToUser(headers=dict, metricId=str, userId=str, reqNum=5)
```

## Share Calculated Metric To Group
```python
shareCalculatedMetricToGroup(headers=dict, metricId=str, imsUserId=str, reqNum=5)
```
* Group Id is represented by the imsUserId variable, please check your instance

## Get Company Calculated Metrics
```python
getCompanyCalculatedMetrics(headers=dict, reqNum = 5)
```

## Update Calculated Metric
```python
updateCalculatedMetric(headers=dict, metricId=str, definition=dict, dataViewId = str, approved =str, reqNum =5)
```
* approved is an optional parameter for if you wish to approve the metric with the changes or not. Set it to a string of `true` or `false`

## Approve Calculated Metric
```python
approveCalculatedMetric(headers=dict, metricId=str, reqNum=5)
```
* filterRemoval - Just the filter ID you wish to remove

## Disapprove Calculated Metric
```python
disapproveCalculatedMetric(headers=dict, metricId=str, reqNum=5)
```

## Delete Calculated Metric
```python
deleteACalculatedMetric(headers=dict, metricId=str, reqNum=5)
```

## Calculated Metric Usage
```python
calculatedMetricUsage(headers=dict, reqNum=5)
```
* Use this to generate a usage report for all your instance's calculated metrics
