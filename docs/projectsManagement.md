# projectsManagement
-----------------------
This module contains all the functions needed to manage projects across your instance and works in tandem with several other modules

## Functionality
* [Copy A Project](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#copy-a-project)
* [Get Project Name](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#get-project-name)
* [Get Project Definition](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#get-project-definition)
* [Get Project Info](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#get-project-info)
* [Get All Project Info](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#get-all-projects-info)
* [Get External References](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#get-external-references)
* [Get Metrics Used In A Project](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#get-metrics-used-in-a-project)
* [Get Filters Used In A Project](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#get-filters-used-in-a-project)
* [Get DataViews Used In A Project](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#get-dataviews-used-in-a-project)
* [Get Date Ranges Used In A Project](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#get-date-ranges-used-in-a-project)
* [Get Calculated Metrics Used In A Project](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#get-calculated-metrics-in-a-project)
* [Get Annotations In A Project](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#get-annotations-in-a-project)
* [Delete A Project](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#delete-a-project)
* [Get Project Usage](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md#get-project-usage)


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
* componentId is the ID of your Project

## Copy A Project
```python
copyAProject(headers=dict, componentId=str, reqNum=5)
```

## Get Project Name
```python
getProjectName(headers=dict, componentId=str, reqNum=5)
```

## Get Project Definition
```python
getProjectDefinition(headers=dict, componentId=str, reqNum=5)
```
* This contains the logic of the project

## Get Project Info
```python
getProjectInfo(headers=dict, componentId=str, reqNum=5)
```
* This generates a basic report of metadata about your project

## Get All Projects Info
```python
getAllProjectaInfo(headers=dict, reqNum=5)
```

## Get External References
```python
getExternalRefernces(headers=dict, componentId=str, reqNum=5)
```
* metadata about which filters, dimensions, metrics, dateranges, dataviews, or annotations are used in the project

## Get Metrics Used In A Project
```python
getMetricsUsedInAProject(headers=dict, componentId=str, reqNum=5)
```

## Get Filters Used In A Project
```python
getFiltersUsedInAProject(headers=dict, componentId=str, reqNum=5)
```

## Get DataViews Used In A Project
```python
getDataViewsUsedInAProject(headers=dict, componentId=str, reqNum=5)
```

## Get Date Ranges Used in A Project
```python
getDateRangesUsedInAProject(headers=dict, componentId=str, reqNum=5)
```

## Get Calculated Metrics In A Project
```python
getCalculatedMetricsInAProject(headers=dict, componentId=str, reqNum=5)
```

## Get Annotations In A Project
```python
getAnnotationsInAProject(headers=dict, componentId=str, reqNum=5)
```

## Delete A Project
```python
deleteAProject(headers=dict, componentId=str, reqNum=5)
```

## Get Project Usage
```python
getProjectUsage(headers=dict, reqNum=5)
```

