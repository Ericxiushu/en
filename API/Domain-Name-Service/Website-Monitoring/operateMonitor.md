# operateMonitor


## 描述
Operation Collection for Monitoring Items, including delete, pause, start, manual recovery and manual switch

## 请求方式
POST

## 请求地址
https://clouddnsservice.jdcloud-api.com/v1/regions/{regionId}/domain/{domainId}/monitorOperate

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**domainId**|String|True| |Domain Name ID|
|**regionId**|String|True| |Region ID to which the instance belongs|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**action**|String|True| |Delete - del, Pause - stop, Start - start, Manually Recover - recover, Manually Switch - switch|
|**ids**|Integer[]|True| |Monitor Item ID|
|**switchTarget**|String|False| |Machine Value of the Monitoring Items, required for manual switch|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|ID of This Request|


## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|BAD_REQUEST|
