# descriptorsManagement
-----------------------
This wrapper is for you to pull a list of your descriptors from your instance of AEP

## Functionality
* [Get Company Descriptors](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/descriptorManagement.md#get-company-descriptors)



## Dependencies
* pandas
* requests
* json
* time
* numpy

## Common Input Parameters
* containerId

## Get Company Descriptors
```python
getCompanyDescriptors(headers=dict, containerId=str, reqNum=5)
```
* containerId will be either `tenant` or `global` depending on your instance and the query.
