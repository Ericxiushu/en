# modifyInstanceCC


## 描述
Set the instance CC defense

## 请求方式
POST

## 请求地址
https://ipanti.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}:setCC

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**instanceId**|String|True| |Instance ID|
|**regionId**|String|True| |Belonging Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**cCSpec**|CCSpec|True| |cc Parameter|

### CCSpec
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**ccProtectMode**|Integer|False| |cc Defense Mode, 0->normal  1->relaxed  2->critical  3->customized|
|**ccThreshold**|Integer|False| |CC Threshold|
|**hostQps**|Integer|False| |When ccProtectMode is a customized mode, specify the protection threshold of each Host|
|**hostUrlQps**|Integer|False| |When ccProtectMode is a customized mode, specify the protection threshold of each Host+URI|
|**ipHostQps**|Integer|False| |When ccProtectMode is a customized mode, specify the protection threshold of each source IP to Host|
|**ipHostUrlQps**|Integer|False| |When ccProtectMode is a customized mode, specify the protection threshold of each source IP to Host+URI|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String| |


## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**404**|NOT_FOUND|
