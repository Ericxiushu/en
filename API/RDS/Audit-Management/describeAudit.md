# describeAudit


## Description
View the audit options of the current instance that have been enabled. If no audit option is enabled for the current instance, it returns an empty array<br>- Support SQL Server Only

## Request method
GET

## Request address
https://rds.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}/audit

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**instanceId**|String|True||RDS instance ID, which uniquely identifies an RDS instance|
|**regionId**|String|True||Region code, with range detailed in [Regions and Availability Zone Comparison Table](../Enum-Definitions/Regions-AZ.md)|

## Request parameter
无


## Return parameter
|Name|Type|Description|
|---|---|---|
|**result**|[Result](##Result)||


### <a name="Result">Result</a>
|Name|Type|Description|
|---|---|---|
|**enabled**|String[]||

## Return code
|Return code|Description|
|---|---|
|**200**|OK|
