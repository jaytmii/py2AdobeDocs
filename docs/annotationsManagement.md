# annotationManagement
-----------------------
This part of the wrapper is for keeping track of annotations made across your projects in CJA

## Functionality
* [Get Annotations](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/annotationsManagement.md#get-annotation)
* [Get All Annotations](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/annotationsManagement.md#get-all-annotations)
* [Get Annotation Tags](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/annotationsManagement.md#get-annotationtags)


## Dependencies
* pandas
* requests
* json
* time
* numpy

## Common Input Parameters
* headers are generated using the auth file and are required for all calls
* reqNum is an optional parameter that can be used to set the number of rertries
* annotationId is the alpha numeric ID assigned to each annotation

## Get Annotation
```python
getAnnotation(headers=dict, annotationId =str, reqNum = int)
```

## Get All Annotations
```python
getAllAnnotations(headers=dict, reqNum = int)
```

## Get AnnotationTags
```python
getAnnotationTags(headers=dict, annotationId =str, reqNum = int)
```
* This will get all tags associated with your specific annotation across all component types.
