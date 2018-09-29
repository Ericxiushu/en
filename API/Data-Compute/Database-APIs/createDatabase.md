# createDatabase


## 描述
Create a user instance database

## 请求方式
POST

## 请求地址
https://xdata.jdcloud-api.com/v1/regions/{regionId}/dwDatabase/{databaseName}

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**databaseName**|String|True| |Database Name|
|**regionId**|String|True| |Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**description**|String|False| |Database Description Information|
|**instanceName**|String|True| |Instance Name|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String| |
|**result**|Result| |

### Result
|名称|类型|描述|
|---|---|---|
|**message**|String| |
|**status**|Boolean| |

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**500**|Internal server error|
