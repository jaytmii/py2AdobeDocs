# filtersManagement
-----------------------
This is for managing your filters on CJA

## Functionality
* [Get Filter](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#get-filter)
* [Get Total Filters Count](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#get-total-filters-count)
* [Get Company Filters](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#get-company-filters)
* [Get Filter Definition](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#get-filter-definition)
* [Copy Filter](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#copy-filter)
* [Get Filter Use Report](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#get-filter-use-report)
* [Share Filter To All](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#share-filter-to-all)
* [Unshare Filter To All](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#unshare-filter-to-all)
* [Share Filter To User](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#share-filter-to-user)
* [Share Filter To Group](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#share-filter-to-group)
* [Approve Filter](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#approve-filter)
* [Disapprove Filter](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#disapprove-filter)
* [Update Filter](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#update-filter)
* [Delete A Filter](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#delete-a-filter)
* [Filter Usage](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md#filter-usage)


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
* filterId is the unique Identifier of the filter

## Get Filter
```python
getFilter(headers=dict, filterId=str, reqNum=int)
```

## Get Total Filters Count
```python
getTotalFiltersCount(headers=dict,  reqNum=int)
```

## Get Company Filters
```python
getCompanyFilters(headers=dict, reqNum=int)
```

## Get Filter Definition
```python
getFilterDefinition(headers=dict, filterId=str, reqNum=int)
```
* This part of the json is the logic for the filter

## Copy Filter
```python
copyFilter(headers=dict, filterId=str, reqNum=int)
```

## Get Filter Use Report
```python
copyFilter(headers=dict, filterId=str, reqNum=int)
```
* Get a report of the usage of the filter across your instance

## Share Filter To All
```python
shareFilterToAll(headers=dict, filterId=str, reqNum=int)
```

## Unshare Filter To All
```python
unshareFilterToAll(headers=dict, filterId=str, reqNum=int)
```

## Share Filter To User
```python
unshareFilterToUser(headers=dict, filterId=str, userId=str,reqNum=int)
```
* userId can be found by checking the accounts identifying information

## Share Filter To Group
```python
shareFilterToGroup(headers=dict, filterId=str, imsUserId=str,reqNum=int)
```
* imsUserId can be found by checking the groups identifying information

## Approve Filter
```python
approveFilter(headers=dict, filterId=str, reqNum=int)
```

## Disapprove Filter
```python
disapproveFilter(headers=dict, filterId=str, reqNum=int)
```

## Update Filter
```python
updateFilter(headers=dict, filterId=str, definition=dict, dataViewId=str, reqNum=int)
```
* definition contains the logic to the filter

## Delete A Filter
```python
deleteAFilter(headers=dict, filterId=str, reqNum=int)
```

## Filter Usage
```python
filterUsage(headers=dict, reqNum=int)
```
* Shows a report of filters by the numbers of projects they are included in