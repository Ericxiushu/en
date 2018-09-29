# assignSecondaryIps


## 描述
Assign secondary IP API to network interface

## 请求方式
POST

## 请求地址
https://vpc.jdcloud-api.com/v1/regions/{regionId}/networkInterfaces/{networkInterfaceId}:assignSecondaryIps

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**networkInterfaceId**|String|True| |networkInterface ID|
|**regionId**|String|True| |Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**force**|Boolean|False|True|When secondary ip is occupied by other interfaces, whether to preempt it or not. false: non-preemption for reallocation, true: preemption for reallocation, default preemption for reallocation. Default value: true|
|**secondaryIpCount**|Number|False| |Assign Automatically Allocated Number of Secondary IP|
|**secondaryIps**|String[]|False| |Assign Allocated Secondary IP Address|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|Request ID|


## 返回码
|返回码|描述|
|---|---|
|**200**|Successful Operation|
|**400**|Request parameter x.y.z is 'xxx', expected one of [yyy,zzz]|
|**404**|Resource Not Found|
