# connectionsManagement
-----------------------
Connections management is primarily for monitoring your connections and staying organized with functionality covering the following areas:

## Functionality
* [Get Company Connections](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/connectionsManagement.md#get-company-connections)
* [Get Single Connection](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/connectionsManagement.md#get-single-connection)
* [Get Company Connections Backfill Report](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/connectionsManagement.md#get-company-connections-backfillreport)
* [Get Company Connections DataSet Report](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/connectionsManagement.md#get-company-connections-dataset-report)
* [Get Data Source Type](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/connectionsManagement.md#get-data-source-type)


## Dependencies
* pandas
* requests
* json
* time

## Common input parameters
* headers are generated using the auth file and are required for all calls
* reqNum is an optional parameter that can be used to set the number of rertries
* connectionId is the unique Id of the connection, usually found in the URL and prefixed with dg_

## Get Company Connections
```python
getCompanyConnections(headers=dict, reqNum = int)
```

## Get Single Connection
```python
getSingleConnection(headers=dict, connectionId=str reqNum = int)
```
* Contains all the logic powering the calculation

## Get Company Connections BackfillReport
```python
getCompanyConnectionsBackfillReport(headers=dict, reqNum=int)
```
* For pulling a count of current backfills by connection

## Get Company Connections DataSet Report
```python
getCompanyConnectionsDataSetReport(headers=dict, reqNum=int)
```
* This will show you all the datasets you have across your connections

## Get Data Source Type
```python
getDataSourceType(headers=dict, reqNum=int)
```
* This will show you all data source types across your company used in all your connections
