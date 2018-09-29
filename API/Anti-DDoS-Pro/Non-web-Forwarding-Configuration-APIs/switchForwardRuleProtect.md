# switchForwardRuleProtect


## 描述
Switch non-web service rules into defense status

## 请求方式
POST

## 请求地址
https://ipanti.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}/forwardRules/{forwardRuleId}:protect

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**forwardRuleId**|String|True| |Forwarding Rule ID|
|**instanceId**|String|True| |Instance ID|
|**regionId**|String|True| |Belonging Region ID|

## 请求参数
无


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String| |


## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**404**|NOT_FOUND|
|**500**|INTERNAL_SERVER_ERROR|
