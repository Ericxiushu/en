# modifyImageAttribute


## 描述
Modify the image information, including name and description; Only allow your personal private image to be operated.


## 请求方式
POST

## 请求地址
https://vm.jdcloud-api.com/1.0.3/regions/{regionId}/images/{imageId}:modifyImageAttribute

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**imageId**|String|True| |Image ID|
|**regionId**|String|True| |Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**description**|String|False| |Description, <a href='https://www.jdcloud.com/help/detail/3870/isCatalog/1'>Refer to the public parameter specification</a>.|
|**name**|String|False| |Name, <a href='https://www.jdcloud.com/help/detail/3870/isCatalog/1'>Refer to the public parameter specification </a>.|


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
