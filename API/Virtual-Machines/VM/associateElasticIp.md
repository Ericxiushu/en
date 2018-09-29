# associateElasticIp


## 描述
The Virtual Machines associates the elastic public IP, and the associating is the IP of the elastic public network corresponding to the primary IP and the intranet primary IP.
A virtual machine can only associate with an EIP (master network card). If the main network card already exists EIP, the error will be returned.


## 请求方式
POST

## 请求地址
https://vm.jdcloud-api.com/1.0.3/regions/{regionId}/instances/{instanceId}:associateElasticIp

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**instanceId**|String|True| |VM ID|
|**regionId**|String|True| |Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**elasticIpId**|String|True| |ID of EIP|


## 返回参数
无


## 返回码
|返回码|描述|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not Found  |
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|
