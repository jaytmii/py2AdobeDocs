# auditLogsManagement
-----------------------
This part of the wrapper is for keeping track of CJA usage. It provides a log of all calls happening across your instance of CJA and can be incredibly useful for pinpointing specific calls that may be slowing down your instance

WARNING: Depending on your traffic these calls will take a long time to pull data. It is highly reccommended that you keep your time periods short.

## Functionality
* [Get Total Audit Logs Count](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/auditLogsManagement.md#get-total-audit-logs-count)
* [Get Company Audit Logs](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/auditLogsManagement.md#get-company-audit-logs)
* [Get Company Audit Logs By Email](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/auditLogsManagement.md#get-company-audit-logs-by-email)
* [Get Company Audit Logs By User Id](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/auditLogsManagement.md#get-company-audit-logs-by-user-id)


## Dependencies
* pandas
* requests
* json
* time
* numpy

## Common Input Parameters
* headers are generated using the auth file and are required for all calls
* reqNum is an optional parameter that can be used to set the number of rertries
* startDate is the start date for your time range and is in a 'YYYY-MM-DD' format
* endDate is the end date for your time range and is in a 'YYYY-MM-DD' format
* userEmail is for querying a single user's CJA usage
* userId is for querying a single user's usage via their Adobe User Id. Should also work on groups if your instance uses service accounts

## Get Total Audit Logs Count
```python
getTotalAuditLogsCount(headers=dict, startDate=str, endDate=str, reqNum=int)
```
* This will give you the total count of audit logs in a requested time period

## Get Company Audit Logs
```python
getCompanyAuditLogs(headers=dict, startDate=str, endDate=str, reqNum=int)
```

## Get Company Audit Logs By Email
```python
getCompanyAuditLogsByEmail(headers=dict, startDate=str, endDate=str, userEmail=str, reqNum=int)
```

## Get Company Audit Logs By User Id
```python
getCompanyAuditLogsByUserId(headers=dict, startDate=str, endDate=str, userId=str, reqNum=int)
```
