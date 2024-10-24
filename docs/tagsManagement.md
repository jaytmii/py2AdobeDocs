# tagsManagement
-----------------------
This module contains all the functions needed to understand your usage of tags in your instance

WARNING: If you have a large number of tags used several of these functions will take a significant amount of time to run

## Functionality
* [Get Total Tags Counts](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/tagsManagement.md#get-total-tags-counts)
* [Get Company Tags](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/tagsManagement.md#get-company-tags)
* [Get Tag Info](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/tagsManagement.md#get-tag-info)
* [Get All Tag Info](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/tagsManagement.md#get-all-tag-info)
* [Retrieve Components By Tag Name](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/tagsManagement.md#retrieve-components-by-tag-name)
* [Retrieve Tags By Component Id](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/tagsManagement.md#retrieve-tags-by-component-id)
* [Remove Tag From Component](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/tagsManagement.md#remove-tag-from-component)
* [Remove Tag From All Components](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/tagsManagement.md#remove-tag-from-all-components)


## Dependencies
* pandas
* requests
* json
* time
* numpy


## Common iInput Parameters
* headers are generated using the auth file and are required for all calls
* reqNum is an optional parameter that can be used to set the number of rertries
* tagId is the unique Id of the Tag
* componentType can currently be `segment`, `project`, or `calculatedMetric`
* componentId is the components uniqueId for the componentType
* tagNames is the name of the tag

## Get Total Tags Counts
```python
getTotalTagsCount(headers=dict, reqNum=int)
```
* A Total count of all tags used in your instance

## Get Company Tags
```python
getCompanyTags(headers=dict, reqNum=int)
```

## Get Tag Info
```python
getCompanyTags(headers=dict, tagId=str, reqNum=int)
```
* Generate a basic report of a singel tag

## Get All Tag Info
```python
getAllTagInfo(headers=dict, reqNum=int)
```
* Similar to other `Company` functions, pulling all tag info

## Retrieve Components By Tag Name
```python
retrieveComponentsByTagName(headers=dict, tagNames=str, componentType=str, reqNum=int)
```
* This will retrieve all projects, segments, or calculatedMetrics used by the tag

## Retrieve Tags By Component Id
```python
retrieveTagsByComponentId(headers=dict, componentType=str, componentId=str, reqNum=int)
```

## Remove Tag From Component
```python
removeTagFromComponent(headers=dict, filterOrCalculatedMetricId=str, componentType=str, reqNum=int)
```
* Can be used to remove from a specific component
* filterOrCalculatedMetricId is the ID for the filter or Calculated Metric Type

## Remove Tag From All Components
```python
removeTagFromAllComponents(headers=dict, tagId=str, reqNum=int)
```
* Used for old tags
