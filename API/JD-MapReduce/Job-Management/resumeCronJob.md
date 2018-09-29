# resumeCronJob


## 描述
Recover a regular task of the job

## 请求方式
POST

## 请求地址
https://idata-jmr-api.jcloud.com/v1/regions/{regionId}/cronJob/{planId}:resume

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**planId**|String|True| |Task ID to be Recovered|
|**regionId**|String|True| |Region ID|

## 请求参数
无


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String| |
|**result**|Result| |

### Result
|名称|类型|描述|
|---|---|---|
|**message**|String| |
|**status**|String| |

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**500**|Internal server error|
