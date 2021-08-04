# Volume - data storage
- When businesses have more data than they are able to process and analyze, they have a volume problem.

- Structured data is organized and stored in the form of values that are grouped into rows and columns of a table.
- Semistructured data is often stored in a series of key-value pairs that are grouped into elements within a file.
- Unstructured data is not structured in a consistent way. Some data may have structure similar to semi-structured data but others may only contain metadata.

- only about 10% is structured
- 10% semi-structured
- 80% everything else

## Introduction to Amazon S3
- Amazon Simple Storage Service (Amazon S3) is the best place to store all of your semistructured and unstructured data.
- Scalabilitly , Security and Performance

- storage underlays the entire data analysis solution. There are three key ways that implementing Amazon S3 as your storage solution can improve your high-volume data analysis solution.
- you can separate the way you store data from the way you process it. This is known as decoupling storage from processing.
- you can access any of these storage locations from any process, in parallel, without negatively impacting other processes.
- becomes a central location to store analytical datasets, providing access for multiple analytic processes at the same time. This allows the solution to avoid the costly process of moving data between the storage system and processing system.

The benefits of Amazon S3 include the following:

    - Store anything
    - Secure object storage
    - Natively online, HTTP access
    - Unlimited scalability 
    - 99.999999999% durability

### Concepts

-  Amazon S3 stores data as objects within buckets.
-  An object is composed of a file and any metadata that describes that file. To store an object in Amazon S3, you upload the file you want to store into a bucket. When you upload a file, you can set permissions on the object and add any metadata.
-  Buckets are logical containers for objects. You can have one or more buckets in your account and can control access for each bucket individually. 

## Introduction to data lakes

- A data lake is an architectural concept that helps you manage multiple data types from multiple sources, both structured and unstructured, through a single set of tools.
- A data lake takes Amazon S3 buckets and organizes them by categorizing the data inside the buckets. It doesn’t matter how the data got there or what kind it is. You can store both structured and unstructured data effectively in an Amazon S3 data lake.
- Out of the dire need for organizing the ever increasing volume of data, data lakes were born.
- Data lakes promise the ability to store all data for a business in a single repository. You can leverage data lakes to store large volumes of data instead of persisting that data in data warehouses.
- Data lakes, such as those built in Amazon S3, are generally less expensive than specialized big data storage solutions.
- That way, you only pay for the specialized solutions when using them for processing and analytics and not for long-term storage.
- Your extract, transform, and load (ETL) and analytic process can still access this data for analytics. 

## Benefits
- Single source of truth
- Store any type of data, regardless of structure
- can be used later for other purposes (AI etc)

## Benefits of datalake in S3
- cost effective
- security and compliance
- many different data collection and ingestion tools 
- categorize and manage data
- meaningful insights

## Amazon EMR and data lakes
- Businesses can place data within a data lake and use their choice of open source distributed processing frameworks, such as those supported by Amazon EMR.
- Apache Hadoop and Spark are both supported by Amazon EMR, which has the ability to help businesses easily, quickly, and cost-effectively implement data processing solutions based on Amazon S3 data lakes.

A data lake on AWS can help you do the following:

- Collect and store any type of data, at any scale, and at low cost
- Secure the data and prevent unauthorized access
- Catalog, search, and find the relevant data in the central repository
- Quickly and easily perform new types of data analysis
- Use a broad set of analytic engines for one-time analytics, real-time streaming, predictive analytics, AI, and machine learning

## AWS Lake Formation
- makes it easy to ingest, clean, catalog, transform, and secure your data and make it available for analysis and machine learning
- central console where you can discover data sources, set up transformation jobs to move data to an Amazon S3 data lake, remove duplicates and match records, catalog data for access by analytic tools, configure data access and security policies, and audit and control access from AWS analytic and machine learning services
- configures underlying AWS services to ensure compliance with your defined policies
- Lake Formation configures the flows, centralizes their orchestration, and lets you monitor the execution of your jobs

## Data Warehouses
- central repository of structured data 
- usually transformed before put in the warehouse
- AWS -> Amazon Redshift
- build to store and query up to petabytes of data
- Amazon Redshift Specturm allows you to query both datalakes and data warehouse
- Amazon EMR: managed hadoop framework
- Whether you use Hadoop on-premises or Amazon EMR, you will use the same tools, with one major exception: Amazon EMR uses its own file system. And that means you can use your Amazon S3 data lake as the data store. So there’s no need to copy data into the cluster, as you would with Hadoop on-premises.
- Amazon EMR File System can catalog data within an Amazon S3 data lake and from an on-premises Hadoop File System at the same time
- The first principle of data analysis is to separate storage from processing. Amazon EMR is a perfect example of this principle.
- A data warehouse is a central repository of structured data from many data sources. This data is transformed, aggregated, and prepared for business reporting and analysis.
- Data flows into a data warehouse from transactional systems, relational databases, and other sources. These data sources can include structured, semistructured, and unstructured data. These data sources are transformed into structured data before they are stored in the data warehouse.
- Data is stored within the data warehouse using a schema. A schema defines how data is stored within tables, columns, and rows.
- Business analysts, data scientists, and decision makers access the data through business intelligence (BI) tools, SQL clients, and other analytics applications. 

## Data marts
- subset of data warehouse
- Data marts only focus on one subject or functional area
- A warehouse might contain all relevant sources for an enterprise, but a data mart might store only a single department’s sources.
- because data marts are generally a copy of data already contained in a data warehouse, they are often fast and simple to implement


| Characteristics       | Data warehouse                                                                                  | Data lake                                                                                                       |
| --------------------- | ----------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Data                  | Relational from transactional systems, operational databases, and line of business applications | Non-relational and relational from IoT devices, websites, mobile apps, social media, and corporate applications |
| Schema                | Designed prior to implementation (schema-on-write)                                              | Written at the time of analysis<br>(schema-on-read)                                                             |
| Price/<br>performance | Fastest query results using higher cost storage                                                 | Query results getting faster using<br>low-cost storage                                                          |
| Data quality          | Highly curated data that serves as the central version of the truth                             | Any data, which may or may not be curated (e.g., raw data)                                                      |
| Users                 | Business analysts                                                                               | Data scientists, data developers, and business analysts (using curated data)                                    |
| Analytics             | Batch reporting, BI, and visualizations                                                         | Machine learning, predictive analytics, data discovery, and profiling.                                          |



- Within AWS, Hadoop frameworks are implemented using Amazon EMR and AWS Glue.
- These services implement the Hadoop framework to ingest, transform, analyze, and move results to analytical data stores.
- Hadoop uses a distributed processing architecture, in which a task is mapped to a cluster of commodity servers for processing.
- The cluster servers frequently use the Hadoop Distributed File System (HDFS) to store data locally for processing.
- One node, designated as the master node, controls the distribution of tasks and can automatically handle server failures.
- Unlike traditional database systems, Hadoop can process structured, semistructured, or unstructured data. This includes virtually any data format currently available.
- you can use Haddop to transform data into formats that allow better integration into your existing data sets. Also, you can store data with or without a schema and perform large-scale ETL operations to transform your data.
- Amazon EMR is the AWS service that implements Hadoop frameworks. 
- Amazon EMR has the ability to implement two different file systems: HDFS or the Elastic MapReduce File System (EMRFS)
- HDFS is distributed storage allowing files to be read and written to clusters of servers in parallel.
- It is helpful to understand the inner workings of an HDFS cluster. An HDFS cluster primarily consists of a NameNode, which manages the file system metadata, and DataNodes, which store the actual data.
- Amazon EMR provides an alternative to HDFS: the EMR File System (EMRFS). 
- EMRFS can catalog data within a data lake on Amazon S3. The time that is saved by eliminating the copy step can dramatically improve performance of the cluster.

