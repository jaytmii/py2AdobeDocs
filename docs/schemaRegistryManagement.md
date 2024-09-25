# schemaRegistryManagement
-----------------------
This covers the stats AEP API. This can be used to get a full list of schemas and other identifying information

WARNING: Most out of the Box functions assume your headers use: `application/vnd.adobe.xdm-v2+json` or some other variant.

## Functionality
* [Get Tenant Id](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/schemaRegistryManagement.md#get-tenant-id)
* [Get Company Descriptors](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/schemaRegistryManagement.md#get-company-descriptors)
* [Delete Descriptors](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/schemaRegistryManagement.md#delete-descriptors)
* [Get Schema Events](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/schemaRegistryManagement.md#get-schema-events)
* [GET Schema Dimensions](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/schemaRegistryManagement.md#get-schema-dimensions)


## Dependencies
* pandas
* requests
* json
* time
* numpy

## Common Input Parameters
* containerId will be either `tenant` or `global` depending on your instance and the query.
* headers are generated using the auth file and are required for all calls
* reqNum is an optional parameter that can be used to set the number of rertries

## Get Tenant Id
```python
getTenantId(headers=dict, reqNum=5)
```

## Get Company Descriptors
```python
getCompanyDescriptors(headers=dict, containerId=str, reqNum=5)
```

## Delete Descriptors
```python
deleteDescriptors(headers=dict, descriptorList=list, reqNum=5)
```
* Run with a list of descriptors

## Get Schema Events
```python
getSchemaEvents(headers=dict, schemaId=str, reqNum=5)
```

## Get Schema Dimensions
```python
getSchemaDimensions(headers=dict, schemaId=str, reqNum=5)
```
