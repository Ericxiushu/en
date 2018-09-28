# deleteSnapshot


## Description
-   Delete a single Cloud Disk snapshot: The snapshot status must be in available or error status.
-   The snapshot is independent from life cycle of the Cloud Disk. Deleting a snapshot does not have any effect on the Cloud Disk that created the snapshot.
-   After the snapshot is deleted, it cannot be recovered. Please be cautious.


## Request method
DELETE

## Request address
https://disk.jdcloud-api.com/v1/regions/{regionId}/snapshots/{snapshotId}

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|
|**snapshotId**|String|True||Snapshot ID|

## Request parameter
None


## Return parameter
|Name|Type|Description|
|---|---|---|



## Return code
|Return code|Description|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|
