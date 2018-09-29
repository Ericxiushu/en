# describeSnapshot


## 描述
Query cloud disk snapshot details

## 请求方式
GET

## 请求地址
https://disk.jdcloud-api.com/v1/regions/{regionId}/snapshots/{snapshotId}

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True| |Region ID|
|**snapshotId**|String|True| |Snapshot ID|

## 请求参数
无


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|Request ID|
|**result**|Result|Cloud Disk Snapshot Details Queried|

### Result
|名称|类型|描述|
|---|---|---|
|**snapshot**|Snapshot| |
### Snapshot
|名称|类型|描述|
|---|---|---|
|**createTime**|String|Creation Time|
|**description**|String|Snapshot Description|
|**diskId**|String|Cloud Disk ID used to create the snapshot|
|**name**|String|Snapshot Name|
|**snapshotId**|String|Cloud Disk Snapshot ID|
|**snapshotSizeGB**|Integer|Snapshot Size, Unit: GiB|
|**status**|String|Snapshot Status, Value: creating, available, in-use, deleting, error_create or error_delete|

## 返回码
|返回码|描述|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|
