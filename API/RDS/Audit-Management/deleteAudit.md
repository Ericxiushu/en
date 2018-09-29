# deleteAudit


## 描述
Disable Database Audit. After the database audit is disabled, the previously generated audit result files are not deleted immediately. The audit result files will be automatically deleted by the system after the expiration date. The default expiration time is 6 months<br>- Support SQL Server Only

## 请求方式
DELETE

## 请求地址
https://rds.jdcloud-api.com/0.2.9/regions/{regionId}/instances/{instanceId}/audit

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**instanceId**|String|True| |RDS instance ID, which uniquely identifies an RDS instance|
|**regionId**|String|True| |Region code, with range detailed in [Regions and Availability Zone Comparison Table](../Enum-Definitions/Regions-AZ.md)|

## 请求参数
无


## 返回参数
无


## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
