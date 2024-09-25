# dataViewsManagement
-----------------------
There is significant functionality provided by the official API endpoints and this wrapper:

## Functionality
* [Get Company DataViews](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#get-company-dataviews)
* [Get Single DataView Info](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#get-single-dataview-info)
* [Get Company DataView Filters](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#get-company-dataview-filters)
* [Get Single DataView Filters Info](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#get-single-dataview-filters-info)
* [Get Company DataViews Usage](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#get-company-dataviews-usage)
* [Get Company DataViews Usage Report](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#get-company-dataviews-usage-report)
* [Create a DataView](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#create-a-dataview)
* [Copy a DataView](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#copy-a-dataview)
* [Delete a DataView](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#delete-a-dataview)
* [Modify DataView Connection](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#modify-dataview-connections)
* [Modify DataView Name](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#modify-dataview-name)
* [Modify DataView Description](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#modify-dataview-description)
* [Modify DataView Timezone](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#modify-dataview-timezone)
* [Modify DataView Session](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#modify-dataview-session)
* [Add DataView Filter](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#add-dataview-filters)
* [Remove DataView Filters](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#remove-dataview-filters)
* [Get DataView Dimensions](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#get-dataview-dimensions)
* [Get DataView Single Dimension](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#get-dataview-single-dimension)
* [Add or Remove Dimensions from a DataView](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#add-or-remove-single-dimension)
* [Bulk Add Or Remove Dimension](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#bulk-add-or-remove-dimension)
* [Change Dimension Name](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#change-dataview-dimension-name)
* [Change Dimension Description](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#change-dataview-dimension-description)
* [Bulk Change Dimension Name](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#bulk-change-dimension-name)
* [Bulk Change Dimension Description](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#bulk-change-dimension-description)
* [Get DataView Metrics](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#get-dataview-metrics)
* [Get DataView Single Metric](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#get-dataview-single-metric)
* [Add or remove a Metric from a DataView](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#add-or-remove-dataview-metric)
* [Change Metric Name](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#change-dataview-metric-name) 
* [Change Metric Description](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#change-dataview-metric-description)
* [Bulk Change Metric Name](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#bulk-change-metric-name)
* [Bulk Change Metric Description](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#bulk-change-metric-description)
* [Bulk Add Or Remove Metric](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md#bulk-add-or-remove-metrics)

## Dependencies
* pandas
* requests
* json
* time
* numpy
* matplotlib

## Common Input Parameters
* headers are generated using the auth file and are required for all calls
* reqNum is an optional parameter that can be used to set the number of rertries
* dataViewId is an alpha numeric string unique identifier for dataviews, it can be found in the URL

## Get Company DataViews
```python
getCompanyDataViews(headers=dict, reqNum = 5)
```

## Get Single DataView Info
```python
getSingleDataViewInfo(headers=dict, dataViewId = str, reqNum = 5)
```

## Get Company DataView Filters
```python
getCompanyDataViewFilters(headers=dict, reqNum = 5)
```

## Get Single DataView Filters Info
```python
getSingleDataViewFilters(headers=dict, dataViewId = str, reqNum = 5)
```

## Get Company DataViews Usage
```python
getCompanyDataViewsUsage(headers=dict, reqNum = 5)
```
* Builds a report based off the number of projects used by each dataView as a proxy for usage

## Get Company DataViews Usage Report
```python
getCompanyDataViews(headers=dict, reqNum = 5)
```
* This is a summation and visualization table of the base report from getCompanyDataViewUsage.

## Create A DataView
```python
createDataView(headers =dict, name = str, description = str,connectionId = str,timezone = str, segmentList = list,numPeriods = int,granularity = str,func = str,  reqNum=5)
```
* name - Refers to the name of the DataView
* description - Refers to the description of the DataView
* connectionId - This is the connection the DataView will use
* timezone - Generally follow known API patterns for setting the timezone, US/Pacific, US/Mountain for example
* segmentList - This is a list of segmentIds to filter the connection by
* numPeriods - This is the number of periods that can pass before the session is ended
* granularity - Set the unit of measure, "MINUTE", "DAY", "HOUR" for example
* func - Set what is being measured by granularity, most common is "INACTIVITY"

## Copy A DataView
```python
copyDataView(headers=dict, dataViewId =str, reqNum = 5)
```

## Delete A DataView
```python
deleteDataView(headers=dict, dataViewId=str)
```

## Modify DataView Connections
```python
modifyDataViewConnection(headers=dict, dataViewId=str, connectionId = str, reqNum = 5)
```

## Modify DataView Name
```python
modifyDataViewName(headers=dict, dataViewId=str, name = str, reqNum = 5)
```

## Modify DataView Description
```python
modifyDataViewDescription(headers=dict, dataViewId=str, description = str, reqNum = 5)
```

## Modify DataView Timezone
```python
modifyDataViewTimezone(headers=dict, dataViewId=str, timezone = str, reqNum = 5)
```

## Modify DataView Session
```python
modifyDataViewSession(headers=dict, dataViewId=str, numPeriod = int, granularity =str, func = str, reqNum = 5)
```

## Add DataView Filters
```python
addDataViewFilters(headers=dict, dataViewId=str, filterAddition = str, reqNum = 5)
```
* filterAddition - Just the filter ID you wish to add
* NOTE: You must have the dimensions and metrics for the filter present in the dataview or the call will fail

## Remove DataView Filters
```python
removeDataViewFilters(headers=dict, dataViewId=str, filterRemoval = str, reqNum = 5)
```
* filterRemoval - Just the filter ID you wish to remove

## Get DataView Dimensions
```python
getDataViewDimensions(headers=dict, dataViewId=str,  reqNum = 5)
```

## Get DataView Single Dimension
```python
getDataViewsSingleDimensions(headers=dict, dataViewId=str, dimensionId = str, reqNum = 5)
```
* dimensionId - From _experience forward is the ID for the dimension

## Add or remove Single Dimension
```python
addOrRemoveDataViewDimension(headers=dict,dataViewId=str,name=str,addOrRemove=str,schemaLocation=str,  reqNum = 5)
```
* name - The name of the Dimension in the UI
* addOrRemove - This will be a string of either "Add" or "Remove" depending on the goal of the user
* schemaLocation - This will be used to reference the dimension. Currently only works for dimension schemas with `variables/` before the rest of the path

## Bulk add or remove Dimension
```python
bulkAddOrRemoveDataViewDimensions(headers =dict, name=list, dataViewId=str, addOrRemove=str, schemaLocation=list)
```
* This works on a single dataView to add a list of dimensions. name and schemaLocation are both lists of strings and must be of equal length

## Change DataView Dimension Name
```python
changeDataViewDimensionName(headers = dict,name = str, dataViewId = str, schemaLocation = str, reqNum = 5)
```

## Change DataView Dimension Description
```python
changeDataViewDimensionDescription(headers = dict,description= str, dataViewId = str, schemaLocation = str, reqNum = 5)
```

## Bulk Change Dimension Name
```python
bulkChangeDataViewDimensionName(headers = dict, name = list, dataViewId=str, schemaLocation=list)
```

## Bulk Change Dimension Description
```python
bulkChangeDataViewDimensionDescription(headers=dict, description=list, dataViewId=str, schemaLocation=list)
```

## Get DataView Metrics
```python
getDataViewMetrics(headers=dict, dataViewId=str, reqNum = 5)
```

## Get DataView Single Metric
```python
getDataViewsSingleMetric(headers=dict, dataViewId=str, metricId=str, reqNum = 5)
```
* metricId - This is usually the same as the schema path, starting with `_experience`

## Add Or Remove DataView Metric
```python
addOrRemoveDataViewMetric(headers=dict,name=str, dataViewId=str,addOrRemove=str,schemaLocation=str, reqNum = 5)
```
* addOrRemove - Must be either, "Add" or "Remove"

## Change DataView Metric Name
```python
changeDataViewMetricName(headers = dict, name = str, dataViewId =str, schemaLocation=str)
```

## Change DataView Metric Description
```python
changeDataViewMetricName(headers = dict, description= str, dataViewId =str, schemaLocation=str)
```
## Bulk change Metric Name
```python
bulkChangeDataViewMetricName(headers = dict, name = list, dataViewId=str, schemaLocation=list)
```

## Bulk change Metric Description
```python
bulkChangeDataViewMetricDescription(headers=dict, description=list, dataViewId=str, schemaLocation=list)
```

## Bulk Add Or Remove Metrics
```python
bulkAddOrRemoveDataViewMetrics(headers =dict, name=list, dataViewId=str, addOrRemove=str, schemaLocation=list)
```
* This works on a single dataView to add a list of dimensions. Name and schemaLocation are both lists of strings and must be of equal length
