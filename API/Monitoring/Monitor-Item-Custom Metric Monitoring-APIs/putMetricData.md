# putMetricData


## 描述
The API is for reporting the custom metric monitoring data, facilitating the user to report the collected time series data to the Monitoring. Original data and aggregated statistical data can be reported in batches. A single request contains up to 50 data points; the data size does not exceed 256k.

## 请求方式
POST

## 请求地址
https://monitor.{regionId}.jdcloud-api.com/v1/customMetrics

无

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**metricDataList**|MetricDataCm[]|False| |Data Parameter|

### MetricDataCm
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**dimensions**|Object|True| |Data dimension, data type is map type, support at least one, up to five tags, no more than 255 bytes in total length, only English, numbers, underlines_, dot., [0-9][a-z] [A-Z] [. _ ] are allowed, others will return err|
|**metric**|String|True| |Metric name, no more than 255 bytes in length, only English, numbers, underlines_, dot., [0-9][a-z] [A-Z] [. _ ] are allowed, others will return err|
|**namespace**|String|True| |Naming space, no more than 255 bytes in length, only English, numbers, underlines_, dot., [0-9][a-z] [A-Z] [. _ ] are allowed, others will return err|
|**timestamp**|Integer|True| |Timestamp for reporting data points only supports 10-bit, second timestamp, the time of the past 30 days cannot be written in|
|**type**|Integer|True| |Data reporting type, 1 is the original value, 2 is aggregated data. When the aggregated data is reported, it is suggested that it shall be reported during the period of 60s, otherwise, it cannot be queried normally.|
|**values**|Object|True| |Metric value collection, the data type must be the map type, key is the data type, value is the data value, when type=1, key only can be “value”, the reported is the original value, when type=2, key can be “avg”, “sum”, “last”, “max”, “min”, “count”, which only support the above types, otherwise it will report an error, value contents are integers or floating point numbers, the largest value is 9223372036854775807, count only supports numbers >=0|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**error**|Object|Error Information|
|**requestId**|String|Request ID|
|**result**|Result| |

### Result
|名称|类型|描述|
|---|---|---|
|**errMetricDataList**|MetricDataList[]| |
|**success**|Boolean|All successful write-ins are true, otherwise are false|
### MetricDataList
|名称|类型|描述|
|---|---|---|
|**errDetail**|String|Error Data Description|
|**errMetricData**|String|Error Data|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|invalid parameter|
|**500**|internal server error|
|**429**|quota exceed|
