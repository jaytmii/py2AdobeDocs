# bulkExportManagement
-----------------------
This wrapper will allow you to track Bulk Export jobs within CJA:

## Functionality
* [Get Bulk Export Jobs List](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/connectionsManagement.md#get-bulk-export-jobs-list)
* [Get Bulk Export Report Type](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/connectionsManagement.md#get-bulk-export-report-type)


## Dependencies
* pandas
* requests
* json
* time
* datetime
* matplotlib

## Common input parameters
* headers are generated using the auth file and are required for all calls
* reqNum is an optional parameter that can be used to set the number of rertries
* imsUserId is specific to the user's account. Any bulk pull will need to loop through a list

## Get Bulk Export Jobs List
```python
getBulkExportJobsList(headers=dict, imsUserId=str | list, reqNum = int)
```

## Get Bulk Export Job Type
```python
getBulkExportReportType(headers=dict, imsUserId=str | list, reqNum = int)
```
* Produces a report with the type of job (daily, monthly, weekly, etc.)

