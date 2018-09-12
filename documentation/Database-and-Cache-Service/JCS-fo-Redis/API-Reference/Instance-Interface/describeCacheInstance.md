# describeCacheInstance

Description: query Redis instance details

- Request method
```xml 
GET https://redis.jdcloud-api.com/v1/regions/{regionId}/cacheInstance/{cacheInstanceId}
```
Name|type|required or not|default|description
---|:--:|:--:|:--:|---:
cacheInstanceId|String|True||Redis instance ID
regionId|String|True||Region ID in the region where the Redis instance is located. At present, Redis includes North China, South China, and eastern China regions. The Region ID is cn-north-1, cn-south-1 and cn-east-2 respectively.

- Request parameter<br>
None

- Return parameter

Name|type|description
---|:--:|---:
cacheInstance|CacheInstance|
requestId|String|

- CacheInstance

Name|type|description
---|:--:|---:
azId|AzId|az information
cacheInstancStatus|String|Instance status: running: running, error: error, creating: creating, changing: charging, deleting: deleting
cacheInstanceClass|String|See Instance Type Code Table for Instance Type code
cacheInstanceDescription|String|instance Description
cacheInstanceId|String|InstanceID
cacheInstanceMemoryMB|Integer|Capacity, in MB
cacheInstanceName|String|Instance Name
charge|Charge|Billing Information
connectionDomain|String|Access Domain
createTime|String|Creation Time
port|Integer|Port
subnetId|String|ID of subnet
vpcId|String|ID of VPC

- AzId

Name|type|description
---|:--:|---:
master|String|Availability Zone ID in the region where the Redis primary instance is located
slave|String|Availability Zone ID in the region where the Redis instance is located

- Charge

Name|type|description
---|:--:|---:
chargeExpiredTime|String|expiration time, the expiration time of Pay-In-Advance resource shall follow the standard of ISO8601 and use UTC time with the format of YYYY-MM-DDTHH:mm:ssZ, Pay-As-You-Go resource field is blank
chargeMode|String|Payment Model, the value shall be: prepaid_by_duration，postpaid_by_usage or postpaid_by_duration, prepaid_by_duration indicates Pay-In-Advance, postpaid_by_usage indicates Pay By Consumption, postpaid_by_duration indicates Pay-As-You-Go by configuration, with the default of postpaid_by_duration
chargeStartTime|String|The start time of billing shall follow the standard of ISO8601 and use the UTC time with the format of YYYY-MM-DDTHH:mm:ssZ
chargeStatus|String|Cost payment status, the value is respectively normal, overdue and arrear

- Error code

Error code|description
---|---:
200|OK
404|NOT_FOUND
