# getPackageId


## Description
Query Crowd Package ID according to device ID

## Request method
GET

## Request address
https://datastar.cn-south-1.jdcloud-api.com/v1/regions/{regionId}/dmp/getPackageId

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**deviceIds**|String|True||MD5 (deviceId), multiple MD5 (deviceId) separated by English commas, note: MD5 result is in lowercase.|


## Return parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String|Request ID, requests are different at each time|
|**result**|Result||


### Result
|Name|Type|Description|
|---|---|---|
|**data**|String|Map<String,String>>, the serialized character string needs to be reconverted before use. Key is deviceId, value is crowd package Id|
|**message**|String|Description Information|
|**status**|Boolean|true is success, false is failure|

## Return code
|Return code|Description|
|---|---|
|**200**|OK|
|**500**|Internal server error|