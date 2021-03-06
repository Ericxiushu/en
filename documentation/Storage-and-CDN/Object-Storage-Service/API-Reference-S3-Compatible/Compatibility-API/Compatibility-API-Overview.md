# Compatible Interface
 Current supported APIs are listed in the below table. Please access  [OSS compatible S3 API documents](https://github.com/jdcloud-cmw/oss/tree/master/S3-API-Document).

|API supported by OSS|API introduction|Description|
|-|-|-|
|GET Service（List Bucket）|Obtain all Buckets under a User|Compatible [GET Service](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTServiceGET.html)|
|PUT Bucket|Create a Bucket, default permission is Private|Compatible  [PUT Bucket](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketPUT.html)|
|HEAD Bucket|Confirm whether a Bucket exists or not and has right to access.<br>If a Bucket exists and has right to access, return 200 OK If the assigned bucket does not exist, return 404 Not Found|Compatible [HEAD Bucket](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketHEAD.html)|
|GET Bucket（List Object）|Obtain the Object information under a Bucket (Compatible Version2)|Compatible [GET Bucket](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/v2-RESTBucketGET.html)|
|DELETE Bucket|Delete the assigned Bucket|Compatible [DELETE Bucket](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketDELETE.html)|
|PUT Object|Upload an Object to OSS|Compatible [PUT Object](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTObjectPUT.html)
|GET Object|Obtain the Meta and data of an Object to obtain all data or use Range to assign to obtain part of the data|Compatible [GET Object](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTObjectGET.html)|
|HEAD Object|Obtain the Meta of an Object|Compatible [HEAD Object](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTObjectHEAD.html)|
|DELETE Object|Delete an Object|Compatible [DELETE Object](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTObjectDELETE.html)|
|Initiate MultiPart Upload|Initialize a MultiPart upload task|Compatible [Initiate MultiPart Upload](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/mpUploadInitiate.html)|
|Upload Part|Upload a Part to OSS|Compatible [Upload Part](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/mpUploadUploadPart.html)|
|Complete MultiPart Upload|Combine multiple parts uploaded into an Object|Compatible [Complete MultiPart Upload](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/mpUploadComplete.html)|
|Abort MultiPart Upload|Abort a MultiPart upload task|Compatible [Abort MultiPart Upload](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/mpUploadAbort.html)|
|List Parts|Obtain information of the part already uploaded by the assigned uploadid|Compatible [List Parts](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/mpUploadListParts.html)|
|List MultiPart Uploads|Obtain the MultiPart task uploaded under a Bucket|Compatible [List MultiPart Uploads](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/mpUploadListMPUpload.html)|
|POST Object|Upload an Object by POST Object|Refer to: [POST Object](./Post-Object-2.md)|
|GET Bucket policy|Obtain policy on the assigned Bucket|Compatible [GET Bucket policy](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketGETpolicy.html)|
|PUT Bucket policy|Add or edit policy on the assigned Buckety|Compatible [PUT Bucket policy](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketPUTpolicy.html)|
|DELETE Bucket policy|Delete policy on the assigned Bucket|Compatible [DELETE Bucket policy](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketDELETEpolicy.html)|
|PUT Bucket acl|Set acl on the assigned Bucket|Compatible [PUT Bucket acl](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketPUTacl.html)|
|GET Bucket acl|Obtain acl on the assigned Bucket|Compatible [GET Bucket acl](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketGETacl.html)|
|PUT Bucket cors|Add CORS rules for the assigned Bucket|Compatible [PUT Bucket cors](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketPUTcors.html)|
|GET Bucket cors|Obtain CORS rules for the assigned Bucket|Compatible [GET Bucket cors](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketGETcors.html)|
|DELETE Bucket cors|Delete CORS rules for the assigned Bucket|Compatible [DELETE Bucket cors](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketDELETEcors.html)|
|PUT Bucket website|Add static website hosting rules for the assigned Bucket (note: The interface is compatible, but the details of rules are different from S3)|Compatible [PUT Bucket website](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketDELETEcors.html)|
|GET Bucket website|Obtain static website hosting rules for the assigned Bucket (note: The interface is compatible, but the details of rules are different from S3)|Compatible [GET Bucket website](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketDELETEcors.html)|
|DELETE Bucket website|Delete static website hosting rules for the assigned Bucket (note: The interface is compatible, but the details of rules are different from S3)|Compatible [DELETE Bucket website](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketDELETEcors.html)|
|Put Object Copy|	Copy an object already existing on OSS into another object|Not support:x-amz-copy-source-if-match，<br>x-amz-copy-source-if-none-match，<br>x-amz-copy-source-if-unmodified-since，<br>x-amz-copy-source-if-modified-since，<br>x-amz-tagging-directive<br>x-amz-storage-class<br>Support:STANDARD/REDUCED_REDUNDANCY<br>Compatible：[PUT Object - Copy](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTObjectCOPY.html)|
|Upload Part Copy|By copying data from an existed Object to upload a Part|Not support:x-amz-copy-source-if-match，<br>x-amz-copy-source-if-none-match，<br>x-amz-copy-source-if-unmodified-since，<br>x-amz-copy-source-if-modified-since<br>Compatible：[Upload Part - Copy](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/mpUploadUploadPartCopy.html)|
|Delete Multiple Objects|Users can delete multiple Objects in the same Bucket by one HTTP request|Not support:version<br>Compatible：[Delete Multiple Objects](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/multiobjectdeleteapi.html)|
|PUT Bucket Replication|Create and modify cross-region replication configuration|Not support:Account，Role，Owner AccessControlTranslation SourceSelectionCriteria<br>Compatible：[PUT Bucket Replication](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketPUTreplication.html)|
|GET Bucket Replication|Return cross-region replication configuration set on Bucket|Compatible：[GET Bucket replication](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketGETreplication.html)|
|Delete Bucket Replication|Delete the enabled cross-region replication configuration, the target Bucket and object remain exist after deletion|Compatible：[Delete Bucket replication](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketDELETEreplication.html)|
|PUT Bucket notification|Assign a Bucket to add NotificationConfiguration|Not support:CloudFunction，Queue<br>Only support: Topic (for details, see [callback notification](../../Operation-Guide/Manage-Bucket/Callback-Notification-2.md))<br>Compatible:[PUT Bucket notification](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketPUTnotification.html)|
|GET Bucket notification|Return NotificationConfiguration set on Bucket|Compatible:[GET Bucket notification](https://docs.aws.amazon.com/zh_cn/AmazonS3/latest/API/RESTBucketGETnotification.html)

