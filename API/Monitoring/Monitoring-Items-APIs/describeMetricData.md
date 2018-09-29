# describeMetricData


## 描述
Get statistics for the specified metric. To get more precise data points, the user can narrow or increase the specified time range.

## 请求方式
GET

## 请求地址
https://monitor.jdcloud-api.com/v1/regions/{regionId}/metrics/{metric}/metricData

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**metric**|String|True| |Metric|
|**regionId**|String|True| |Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**endTime**|String|False| |Query end time of time range, UTC time, format: 2016-12- yyyy-MM-dd'T’HH:mm:ssZ (if it is blank, which shall be obtained by computing startTime and timeInterval)|
|**resourceId**|String|True| |Uuid of Resource|
|**serviceCode**|String|True| |Type of resource, taking values such as vm, lb, ip, and database|
|**startTime**|String|False| |Query start time of time range, UTC time, format: yyyy-MM-dd'T’HH:mm:ssZ (current time by default, if it is earlier than 30d, it will be reset to 30d)|
|**tags**|TagFilter[]|False| |Custom Tag|
|**timeInterval**|String|False| |Time interval: 1h, 6h, 12h, 1d, 3d, 7d, 14d, fixed time interval, fill in at least one of timeInterval and endTime|

### TagFilter
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**key**|String|True| |Tag Key|
|**values**|String[]|True| |Tag Value|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|Request ID|
|**result**|Result| |

### Result
|名称|类型|描述|
|---|---|---|
|**metricDatas**|MetricData[]| |
### MetricData
|名称|类型|描述|
|---|---|---|
|**data**|DataPoint[]| |
|**metric**|Metric| |
### DataPoint
|名称|类型|描述|
|---|---|---|
|**timestamp**|Integer|Time Stamp|
|**value**|String|Value|
### Metric
|名称|类型|描述|
|---|---|---|
|**calculateUnit**|String|Computing Unit of Metric, such as bit/s, %, and k|
|**metric**|String|English Identifier of Monitoring Item|
|**metricName**|String|Name of Monitoring Item|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|invalid parameter|
|**500**|internal server error|
