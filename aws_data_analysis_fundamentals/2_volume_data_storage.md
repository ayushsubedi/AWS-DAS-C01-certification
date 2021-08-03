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
 
