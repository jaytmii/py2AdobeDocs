# auth
-----------------------
This part of the wrapper is for authenticating or pulling specific data from your generated config file. If you have questions on the config please go back to the getting started section. 

WARNING: Please make sure that anytime you reference your config file or your private key (if using JWT) your directory is set correctly.

Additionally please make sure you have your integration set up at https://developer.adobe.com/console/home

## Functionality
* [OAuth S2S Auth](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/auth.md#oauth-s2s-auth)
* [JWT Auth](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/auth.md#jwt-auth)
* [AA JWT Headers](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/auth.md#aa-jwt-headers)
* [CJA JWT Headers](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/auth.md#cja-jwt-headers)
* [CJA OAuth Headers](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/auth.md#cja-oauth-headers)
* [AEP OAuth Headers](https://github.com/jaytmii/py2AdobeDocs/blob/main/docs/auth.md#aep-oauth-headers)


## Dependencies
* pandas
* requests
* json
* time
* configparser
* jwt
* authlib OAuth2Session
* numpy

## Common Input Parameters
* yourConfigFile
* scopesForAuth
* access_token

## OAuth S2S Auth
```python
oauthS2SAuth(yourConfigFile=str, scopesForAuth=str)
```
* yourConfigFile will be in the form of fileName.config
* scopesForAuth will be referenced via the generated config, so s2s_aa_scopes, jwt_scopes, etc. You need to use the following syntax for the scopesForAuth variable replacing JWT for the first section or S2S depending on your method of auth:
* AA: `s2s_aa_scopes`
* CJA: `s2s_cja_scopes + s2s_aep_scopes`
* AEP: `s2s_aep_scopes`
* I/O: `s2s_io_scopes`

## JWT Auth
```python
jwtAuth(yourConfigFile=str)
```

## AA JWT Headers
```python
aaJwtHeaders(yourConfigFile=str, access_token =str)
```
* Will fully generate your headers for making calls using JWT, pass the access_token generated from the auth function


## CJA JWT Headers
```python
cjaJwtHeaders(yourConfigFile=str, access_token =str)
```

## CJA OAuth Headers
```python
cjaOauthHeaders(yourConfigFile=str, access_token =str)
```

## AEP OAuth Headers
```python
aepOauthHeaders(yourConfigFile=str, access_token =str, acceptHeader=str)
```
* acceptHeader is for functions that require variant accept headings to tailor your query