# deleteNamespace


## 描述
Delete namespace; if there are other subordinate resources associated with it, it is not allowed to delete it

## 请求方式
DELETE

## 请求地址
https://streamcompute.jdcloud-api.com/v1/regions/{regionId}/namespace

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**namespaceId**|Integer|True|||


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|[Result](##Result)||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**status**|Boolean|Delete the namespace successful marker|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**500**|INTERNAL_ERROR|
|**400**|INTERNAL_ERROR|