# modifyContainerAttribute


## 描述
Modify the container name and description.


## 请求方式
PATCH

## 请求地址
https://nc.jdcloud-api.com/v1/regions/{regionId}/containers/{containerId}:modifyContainerAttribute

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**containerId**|String|True| |Container ID|
|**regionId**|String|True| |Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**description**|String|False| |Container description; the description must be specified|
|**name**|String|False| |Container Name|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String| |


## 返回码
|返回码|描述|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|
