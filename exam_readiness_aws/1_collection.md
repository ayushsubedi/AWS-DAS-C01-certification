# Domain 1: Collection

- focuses on ingesting data from transactions, logs, IOT devices
- allows developers to ingest a wide variety of data, structured, semistructured and unstructured, at any speed from batch to streaming
- 18% of the exams will focus on this topic

## Subdomains

1. determine the operational characteristics of the collection system
2. select a collection system that handles the frequency, volume and source of data
3. select a collection system that addresses the key properties of data, such as order, format, and compression


## 1: Determine the operational characteristics of the collection system

- Pipeline vulnerability (vulnerability in pipeline)
- to decrease pipeline vulnerability it is a good idea to decouple data analytics pipeline
- much less expensive
- each tool can be built to exact specifications, avoid overprovisioning, and handle failure gracefully
- failure handling is important as losing large data sets can be difficult to recover

## Assessing fault tolerance and data persistence of the collection system

### Amazon Kinesis Data Streams
- Kinesis Producer Library -> Amazon Kinesis Data Streams -> Kinesis Consumer Library
- Fault Tolerance and data persistence
  - KPL sends multiple records to stream per request. If single record fails, it is automatically added back to the KPL buffer and retried. The failure of one record does not impact the processing of other records in the request. 
  -  
