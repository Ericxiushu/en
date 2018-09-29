# modifyNetworkInterface


## 描述
Modify elastic network interface APIs

## 请求方式
PATCH

## 请求地址
https://vpc.jdcloud-api.com/v1/regions/{regionId}/networkInterfaces/{networkInterfaceId}

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**networkInterfaceId**|String|True| |networkInterface ID|
|**regionId**|String|True| |Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**description**|String|False| |Description, allow all characters under UTF-8 coding, not exceeding 256 characters|
|**networkInterfaceName**|String|False| |Elastic Network Interface name, only allows Chinese, numbers, capital and lowercase letters, English underline “_” and line-through “-”, must provide a name which cannot exceed 32 characters|
|**securityGroups**|String[]|False| |To replace the Security Group with mode update of the original Security Group. If the Security Group ID list is updated, a maximum of 5 Security Groups can be done|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|Request ID|


## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|Request parameter x.y.z is 'xxx', expected one of [yyy,zzz]|
|**404**|Resource Not Found|
