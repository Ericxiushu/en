# modifyBackupPolicy


## 描述
Modify backup policy

## 请求方式
POST

## 请求地址
https://mongodb.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}/backupPolicy

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**instanceId**|String|True| |Instance ID|
|**regionId**|String|True| |Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**preferredBackupTime**|String|True| |Backup Time, Format: HH:mmZ- HH:mmZ, only integral point allowed with interval of 1 hour.|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String| |
|**result**|Result| |

### Result
|名称|类型|描述|
|---|---|---|
|**backupRetentionPeriod**|String| |
|**preferredBackupPeriod**|String| |
|**preferredBackupWindow**|String| |

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
