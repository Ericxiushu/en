# describeInstances


## 描述
Search the instance list

## 请求方式
GET

## 请求地址
https://ipanti.jdcloud-api.com/v1/regions/{regionId}/instances

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True| |Belonging Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**name**|String|False| |Instance Name, Fuzzy Matching Available|
|**pageNumber**|Integer|False| |Page Number: 1 by default|
|**pageSize**|Integer|False| |Paging Size: 20 by default; value range [10, 100]|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String| |
|**result**|Result| |

### Result
|名称|类型|描述|
|---|---|---|
|**dataList**|Instance[]| |
|**totalCount**|Integer| |
### Instance
|名称|类型|描述|
|---|---|---|
|**abovePeakCount**|Integer|Frequency of Over Peak Value|
|**businessBitslimit**|Integer|Business Bandwidth|
|**carrier**|String|ISP Line, i.e. UNICOM and TELECOM|
|**ccProtectMode**|Integer|cc Defense Mode, 0->normal  1->critical  2->relaxed  3->customized|
|**ccProtectStatus**|Integer|cc enabling status, 0->disabled  1->enabled|
|**ccSpeedLimit**|Integer|cc defense mode has the same speed limit as customized mode|
|**ccSpeedPeriod**|Integer|cc defense mode has the same speed limit period as customized mode|
|**ccThreshold**|Integer|CC Threshold|
|**chargeStatus**|String|PAID|ARREARS|EXPIRED|
|**createTime**|Integer|Instance Creation Time|
|**elasticTriggerCount**|Integer|Times of Triggering Elastic Bandwidth|
|**expireTime**|Integer|Instance Expiration Time|
|**hostQps**|Integer|The protection threshold of each Host when ccProtectMode is a customized mode|
|**hostUrlQps**|Integer|The protection threshold of each Host+URI when ccProtectMode is a customized mode|
|**inBitslimit**|Integer|Minimum Bandwidth|
|**instanceId**|Integer|Instance ID|
|**ipBlackList**|String[]|IP Blacklist|
|**ipBlackStatus**|Integer|IP Blacklist Status, 0->disabled  1->enabled|
|**ipHostQps**|Integer|The protection threshold of each source IP to Host when ccProtectMode is a customized mode|
|**ipHostUrlQps**|Integer|The protection threshold of each source IP to Host+URI when ccProtectMode is a customized mode|
|**ipWhiteList**|String[]|IP White List|
|**ipWhiteStatus**|Integer|IP White List Status, 0->disabled  1->enabled|
|**name**|String|Instance Name|
|**pin**|String|User Pin|
|**resilientBitslimit**|Integer|Elastic Bandwidth|
|**resourceId**|String|Resource ID, used during upgrade and renewal|
|**ruleCount**|Integer|Non-web Service Rules|
|**securityStatus**|String|SAFE|CLEANING|BLOCKING|
|**urlWhitelist**|String[]|url White List|
|**urlWhitelistStatus**|Integer|url White List Status, 0->disabled  1->enabled|
|**webRuleCount**|Integer|Web Service Rules|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
