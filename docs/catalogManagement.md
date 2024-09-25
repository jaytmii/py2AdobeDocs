# catalogManagement
-----------------------
This wrapper is for the catalog API that Adobe provides. Generally for batches, datasets, and tags.

WARNING: Most out of the Box functions assume your headers use: `application/vnd.adobe.xdm-v2+json`

## Functionality
* [Get Company DataSets](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/catalogManagement.md#get-company-datasets)
* [Get Company Schemas By DataSet Id](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/catalogManagement.md#get-company-schemas-by-dataset-id)
* [Delete DataSet](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/catalogManagement.md#delete-dataset)



## Dependencies
* pandas
* requests
* json
* time
* numpy

## Common Input Parameters
* schemaId - This is the unique identifier for the schema
* dataSetId - This is the unique identifier for the dataset
* headers are generated using the auth file and are required for all calls
* reqNum is an optional parameter that can be used to set the number of rertries

## Get Company Datasets
```python
getCompanyDataSets(headers=dict, reqNum=5)
```

## Get Company Schemas By DataSet Id
```python
getCompanySchemasByDataSetId(headers=dict, schemaId=str, reqNum=5)
```

## Delete DataSet
```python
deleteDataSet(headers=dict, dataSetId=str, reqNum=5)
```

