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
