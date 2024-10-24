# py2AdobeDocs
Your guide to using the py2Adobe package to get started as well as understanding how to leverage all the prebuilt functions
-----------------------
For initial access to this you mus be permissioned to use both CJA's API and AEP.

To setup your integration please follow this link: [Adobe Developer Console](https://developer.adobe.com/console/home)

## Getting Started
These Docs will be organized generally by API that they wrap, to start with lets discuss how to import correctly. First install using pip with the following command:

```python
pip install py2Adobe
```

Follow that up with the import function

```python
import py2Adobe as p2a
```
Before executing any calls you must first generate your config file. This can be done by calling the config generator module like below if you are not using Jupyter Notebooks:

```python
inputs = p2a.configGenerator.AuthType()
import os
## Wherever you want your config to live. Single slashes if on Mac
os.chdir('C:\\Users\\userName\\py2Adobe')
p2a.configGenerator.createConfig(inputs)
```
You will be prompted to fill in several parts from your integration, it is pretty straightforward. Currently until 2025 you'll be prompted for JWT and S2S. Both options are available until Adobe deprecates them.

Lastly lets cover authentication basics. You need to generate an access token and your headers and that will vary by tool. Please see the auth docs below for details on which scope for which token, but your code should look like so with generation of an access token and then placing that in your headers:

```python
access_token = p2a.auth.oauthS2SAuth(yourConfigFile, scopesForAuth)
headers = p2a.auth.cjaOauthHeaders(yourConfigFile, access_token)
```
Please see the auth docs below to better understand how to format each of the parameters for the access token.

Now that you are up and running you can follow a link to any of the below for the API specific methods:
## CJA 
* [annotationManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/annotationsManagement.md)
* [auditLogsManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/auditLogsManagement.md)
* [auth](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/auth.md)
* [bulkExportManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/bulkExportManagement.md)
* [connectionsManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/calculatedMetricsManagement.md)
* [consumptionManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/consumptionManagement.md)
* [dataViewsManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataViewsManagement.md)
* [dataScienceManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/dataScienceManagement.md)
* [filtersManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/filtersMangement.md)
* [projectsManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/projectsManagement.md)
* [reportingManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/reportingManagement.md)
* [sharesManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/sharesManagement.md)
* [tagsManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/tagsManagement.md)

## AEP
* [schemaRegistryManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/schemaRegistryManagement.md)
* [catalogManagement](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/catalogManagement.md)


## Bug Reporting
If you want to report an issue with the package functions you can use GitHub's Issues system for this repo to submit or submit via this [email](py2Adobe@gmail.com). Please be as detailed as possible and thank you!
