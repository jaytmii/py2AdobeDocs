# sharesManagement
-----------------------
This module contains all the functions needed to understand what has been shared in your instance you

## Functionality
* [Get Components Shared By Current User](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/sharesManagement.md#get-components-shared-by-current-user)
* [Get Components Shared With Current User](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/sharesManagement.md#get-components-shared-with-current-user)


## Dependencies
* pandas
* requests
* json
* time
* numpy


## Common Input Parameters
* headers are generated using the auth file and are required for all calls
* reqNum is an optional parameter that can be used to set the number of rertries
* componentType can currently be `segment`, `project`, or `calculatedMetric`

## Get Components Shared By Current User
```python
getComponentsSharedByCurrentUser(headers=dict, reqNum=int)
```

## Get Components Shared With Current User
```python
getSharedComponentsForCurrentUser(headers=dict, componentType=str, reqNum=int)
```



