# Velocity - data processing

- When businesses need rapid insights from the data they are collecting, but the systerms in place simply cannot meet the need, there is a velocity problem.
- The speed at which data is being generated is ever accelearating. Emails, photos, Twitter, etc are all examples of data that is being generated rapidly and must be collected, processed, analyzed and stored
- The collection and processing of data are combined into a single concept known as data processing.

- Data processing means the collection and manipulation of data to produce meaningful information. Data collection is divided into, data collection and processing.
- Data processing is vital to any data system. Data processing defines the methods that are used to collect data and present it to storage or analytic mechanisms.


## Batch processing
- processing content in batches
- when you have a lot of data to process and you need to process at certain intervals
- ex at certain intervals or when you reach certain volume
- log, financial data etc
- deep insight
- **customer fraud analysis

### Scheduled batch processing
- same amount of data
- workload is predictible

### Periodic
- once a certain amount of data is collected

They may still need high velocity. Example, airlines. The airplane must know if it is ready for another flight.

- mostly only one service (single application to collect and store and analyze)
- Amazon EMR (managed hadoop framework uses hive and spark)
- entire dataset is being used
- deep insights
- latency can be minutes to hour, depending on the analysis being performed



## Stream processing
- processing data generated continiously
- in small size
- realtime feedback
- continious feedback
- ecommerce purchase, clickstreams, gaming etc
- initial insight 
- **streaming data fraud prevention credit card: sms

### Realtime
- within millisecond

### Near realtime
- within minutes

- multiple service
- one service to ingest, another to process, another to load it to analytical datastore
- kinesis data firehose, kinesis data streams, amazon kinesis data analytics (allows analysis in rolling time periodm usually for aggregation)
- latency is milliseconds to seconds

________________________

- in real world, it might not be that easy
- retail chain trying to analyze point of sale application:
  - each location sending data thoughout the day
  - rapid processing until 1:15 am 
  - slow collection, rapid processing
  - batch processing

- advertising company using social media for product trends
  - once collected, it must be collected just as fast
  - rapid collection followed by rapid processing
  - streaming solution 

___________________________

Batch: Velocity is very predictable with batch processing. It amounts to large bursts of data transfer at scheduled intervals.

Periodic: Velocity is less predictable with periodic processing. The loss of scheduled events can put a strain on systems and must be considered.

Near real-time: Velocity is a huge concern with near real-time processing. These systems require data to be processed within minutes of the initial collection of the data. This can put tremendous strain on the processing and analytics systems involved.

Real-time: Velocity is the paramount concern for real-time processing systems. Information cannot take minutes to process. It must be processed in seconds to be valid and maintain its usefulness.

Batch and periodic: Once the data has been collected, processing can be done in a controlled environment. There is time to plan for the appropriate resources.

Near real-time and real-time: Collection of the data leads to an immediate need for processing. Depending on the complexity of the processing (cleansing, scrubbing, curation), this can slow down the velocity of the solution significantly. Plan accordingly.

Data acceleration: The rate at which large collections of data can be ingested, processed, and analyzed. Data accelearation is not constant and comes in bursts. Example hashtag trending on twitter for which the system needs to be capable to process it.

|            | Batch data processing                                             | Stream data processing                                                                               |
| ---------- | ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Data scope | Queries or processing over all or most of the data in the dataset | Queries or processing over data within a rolling time window, or on just the most recent data record |
| Data size  | Large batches of data                                             | Individual records or micro batches consisting of a few records                                      |
| Latency    | Minutes to hours                                                  | Seconds or milliseconds                                                                              |
| Analysis   | Complex analytics                                                 | Simple response functions, aggregates, and rolling metrics                                           |


## Introduction to batch data processing

- Batch processing is often thought of as a slow process. This is not the case. 
- Batch processing must quickly and efficiently consume a huge amount of data all at once.
- Batch data processing provides companies with the ability to dive deep into the data they have collected to produce complex analytics that simply cannot be achieved using streaming analytics.
- With modern architectures, you can optimize batch processing systems to the frequency and size of the batches you’re processing. 
- execution of series of programs or jobs without intervention
  - data is collected asynchronously (when a condition is met)
  - frequency and size of batch can be managed with AWS
  - traditional on premise system which is centralized almost fails to keep up with the velocity of today
- Amazon EMR decouples collection and processing
- you can also run other popular distributed frameworks such as Apache Spark, HBase, Presto, and Flink in EMR.
- decoupling the collection system from the processing system. This is accomplished by implementing one of two common frameworks: Hadoop or Apache Spark. Both frameworks process high-velocity data but they do it in different ways.
- Amazon EMR notebooks provide a serverless development and collaboration environment for one-time querying and exploratory analysis. You can manipulate the data and generate data plots using rich graphical tools. Amazon EMR notebooks monitor your jobs and even help you debug code from the notebooks.



### Hadoop
- scalable storage and batch data processing system
- running EMR configures the clusters of EC2 instances to serve as a single distributed storage and processing
  - provides speed
  - fault tolerance
  - scale
- simultaniously ingesting and processing all type of data (structured/unstructured)

#### Hadoop Common
Hadoop Common is the set of Java utilities and libraries that support the other Hadoop modules. These libraries help abstract the file system from the processing components. These Java files and scripts are required to start Hadoop.

#### HDFS
Hadoop Distributed File System (HDFS) is the distributed file system that stores the data in a high-throughput environment of community nodes. This architecture ensures very high aggregate bandwidth access to application data..

#### Hadoop YARN
Hadoop YARN is the resource management framework responsible for scheduling and executing processing jobs.

#### Hadop MapReduce
Hadoop MapReduce is a YARN-based system that allows for parallel processing of large data sets on the cluster.



### Apache Spark
- competing product
- in memory caching and optimized execution
- avoids writing data to storage

Both Spark and hadoop support:
- General batch processing
- Streaming Aanalytics
- Machine learning
- Graph databases
- Ad hoc queries

### Amazon EMR with other AWS services
- Data sources -> S3 -> AWS lambda (create a program to run every 4 hour) -> send them to EMR for aggregation and load -> Redshift

OR

- AWS Glue
- simplifies data discovery, conversion, mapping, etc etc. basically processing
- same data architecture but instead of EMR we use glue

## Introduction to stream data processing

- amount of data being transferred and size is not constant
- excel at working with data with value that diminises over time
- alarms
- first benefit: control
- producers and consumers
- multiple stream can be combined into a single stream
- ability to preserve the order of data
- consumer: will process the incoming stream
- parallel consumption lets multiple consumers work simultaniously

#### AWS
- Amazon Kinesis
- makes it easy to collect, process and analyze streaming data
- cost effective, scale etc

#### AWS Kinesis
- AWS Kinesis data firehose
  - Amazon Kinesis Data Firehose is the easiest way to capture, transform, and load data streams into AWS data stores for near real-time analytics with existing business intelligence tools.  
- AWS Kinesis data streams
  - Amazon Kinesis Data Streams enables you to build custom, real-time applications that process data streams using popular stream processing frameworks.  
- AWS Kinesis data analytics
  - Amazon Kinesis Data Analytics is the easiest way to process data streams in real time with SQL or Java without having to learn new programming languages or processing frameworks. 
- AWS Kinesis video streams (securily stream video)
  - Amazon Kinesis Video Streams makes it easy to securely stream video from connected devices to AWS for analytics, machine learning (ML), and other processing. 

Sensor Data -> Streaming Collection (using firehose) -> Stream Processing Layer (Kinesis Data analytics -> Firehose) -> S3 -> Athena -> QuickSight

- you can filter/not filter depending on use case
- you can also use AWS glue to connect multiple S3
- you can store raw streams and batch analyze them too
