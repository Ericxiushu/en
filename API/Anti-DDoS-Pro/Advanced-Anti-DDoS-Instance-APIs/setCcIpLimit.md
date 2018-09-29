# setCcIpLimit


## 描述
Set the speed limit of each Ip of instance CC defense

## 请求方式
POST

## 请求地址
https://ipanti.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}:setCcIpLimit

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**instanceId**|String|True| |Instance ID|
|**regionId**|String|True| |Belonging Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**cCSpec**|CcIpLimitSpec|True| |cc Parameter|

### CcIpLimitSpec
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**ccSpeedLimit**|Integer|False| |Speed Limit of Each CC Defense IP|
|**ccSpeedPeriod**|Integer|False| |Speed Limit Statistic Period of Each CC Defense IP|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String| |


## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**404**|NOT_FOUND|
