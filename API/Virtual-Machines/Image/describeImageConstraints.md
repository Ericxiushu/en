# describeImageConstraints


## Description
查询镜像的实例规格限制。<br>
This interface allows you to view the type of specifications that are not supported by the image. Only the public image,  the third-party image has a specification type restriction,  and the private image of the individual does not have this limit.


## Request method
GET

## Request address
https://vm.jdcloud-api.com/v1/regions/{regionId}/images/{imageId}/constraints

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**imageId**|String|True||Image ID|
|**regionId**|String|True||Region ID|

## Request parameter
None


## Return parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String||
|**result**|[Result](##Result)||


### <a name="Result">Result</a>
|Name|Type|Description|
|---|---|---|
|**imageConstraints**|[ImageConstraint](##ImageConstraint)|image restriction|
### <a name="ImageConstraint">ImageConstraint</a>
|Name|Type|Description|
|---|---|---|
|**imageId**|String|Image ID|
|**imageInstanceTypeConstraint**|[ImageInstanceTypeConstraint](##ImageInstanceTypeConstraint)|Specification limit for instance type created by image|
### <a name="ImageInstanceTypeConstraint">ImageInstanceTypeConstraint</a>
|Name|Type|Description|
|---|---|---|
|**constraintsType**|String|Restricted specification type. excludes: exclude specified instance types; includes: only the specified instance type is included,  which is not supported temporarily|
|**instanceTypes**|String[]|Instance type list|

## Return code
|Return code|Description|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|