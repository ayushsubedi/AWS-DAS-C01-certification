# Variety - data structure and types

- When your business becomes overwhelmed by the sheer number of data sources to analyze and you cannot find systems to perform the analytics, you know you have a variety problem.

## Introduction to source data storage
- A data source can be just about anything—a folder on a file server, database, web page, and even a wearable device can be considered a data source.
- Some data sources use a schema to organize content and indexes to improve performance. Others organize data in a more flexible way and are called schemaless. Schemaless data sources still use indexes to improve performance. 
- Three data source:
  - Structured
    - Transactional database (heavy write and update)
    - Analytical database (heavy read) 
  - Semi-structured
  - Unstructured
    -  stored as files
    -  no pre defined schema
    -  pdfs
    -  maybe, little to no text
    -  preprocessing is necessary (maybe add tags, or catalog the data)

Structured data is stored in a tabular format, often within a database management system (DBMS). This data is organized based on a relational data model, which defines and standardizes data elements and their relation to one another. Data is stored in rows, with each row representing a single instance of a thing (for example, a customer). These rows are well understood due to the table schema, which explains what each field in the table represents. This makes structured data easy to query.
The downside to structured data is its lack of flexibility. Let’s say that you have decided you want to track the age of your customers. You must reconfigure the schema to allow for this new data, and you must account for all records that don’t have a value for this new field. It is not impossible, but it can be a very time-consuming process.
Examples of structured data applications include Amazon RDS, Amazon Aurora, MySQL, MariaDB, PostgreSQL, Microsoft SQL Server, and Oracle.

Semistructured data is stored in the form of elements within a file. This data is organized based on elements and the attributes that define them. It doesn't conform to data models or schemas. Semistructured data is considered to have a self-describing structure. Each element is a single instance of a thing, such as a conversation. The attributes within an element define the characteristics of that conversation. Each conversation element can track different attributes. This makes semistructured data quite flexible and able to scale to meet the changing demands of a business much more rapidly than structured data.
The trade-off is with analytics. It can be more difficult to analyze semistructured data when analysts cannot predict which attributes will be present in any given data set.
Examples of semistructured data stores include CSV, XML, JSON, Amazon DynamoDB, Amazon Neptune, and Amazon ElastiCache.

Unstructured data is stored in the form of files. This data doesn't conform to a predefined data model and isn't organized in a predefined manner. Unstructured data can be text-heavy, photographs, audio recordings, or even videos. Unstructured data is full of irrelevant information, which means the files need to be preprocessed to perform meaningful analysis. This can be done in many ways. For example, services can add tags to the data based on rules defined for the types of files. The data can also be cataloged to make it available to query services.
Examples of unstructured data include emails, photos, videos, clickstream data, Amazon S3, and Amazon Redshift Spectrum.


#### How do you incorporate all these?


## Introduction to structured data stores
- relational database (ACID)
- A process known as normalization helps a business take flat-file data and turn it into a relational database. Normalization is a set of rules that work together to reduce redundancy, increase reliability, and improve the consistency of data storage.
- OLTP vs OLAP
- why two different systems?
- comes down to how the resources supporting the db, is being used?
- write operation vs read operation
- use same resources but different 
- you can optimize for one, one is usually sacrified
- OLTP -> scheduled transformed ETL -> OLAP

### OLTP
Online transaction processing (OLTP) databases, often called operational databases, logically organize data into tables with the primary focus being on the speed of data entry. These databases are characterized by a large number of insert, update, and delete operations.
All decisions about the organization of data and storage of attributes is based on ensuring rapid data entry and updates. The effectiveness of an OLTP system is often measured by the number of transactions per second.

### OLAP
Online analytical processing (OLAP) databases, often called data warehouses, logically organize data into tables with the primary focus being the speed of data retrieval through queries. These databases are characterized by a relatively low number of write operations and the lack of update and delete operations.

All decisions about the organization of data and storage of attributes are based on the types of queries and other analytics that will be performed using the data. The effectiveness of an OLAP system is often measured by the response time of query results.


| Characteristic | OLTP                                                 | OLAP                                    |
| -------------- | ---------------------------------------------------- | --------------------------------------- |
| Nature         | Constant transactions (queries/updates)              | Periodic large updates, complex queries |
| Examples       | Accounting database, online retail transactions      | Reporting, decision support             |
| Type           | Operational data                                     | Consolidated data                       |
| Data retention | Short-term (2-6 months)                              | Long-term (2-5 years)                   |
| Storage        | Gigabytes (GB)                                       | Terabytes (TB)/petabytes (PB)           |
| Users          | Many                                                 | Few                                     |
| Protection     | Robust, constant data protection and fault tolerance | Periodic protection                     |

#### Retrival of data
- Indexed tables return query results much faster
- much faster retrival time (row based indexing)
- OLAP: most common queries: aggregate
- row based index might not make sense in OLAP (every col of very row is loaded)
- columnal indexing changes the way index are build, they index column by column
- by indexing column, the query only needs to load the specific column
- other key advantage - > compressing the data
- also, columnar based index only stores unique element -> amazing compression
- significantly reduces data waste

### AWS 
- Amazon RDS (both for OLAP and OLTP buy only row based index)
  - Easy to set up operate and scale
  - cost efficient and scaleable capacity
- Redshift (for OLAP with column based index)  
