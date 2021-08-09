# S3 storage classes
https://aws.amazon.com/s3/storage-classes/

- Amazon S3 Standard - General Purpose
  - 99.999999999% high durability across multiple AZ
  - 99.99% availability over a given year
  - sustain 2 concurrent facility failure
  - gaming, data analytics, applications etc

- Amazon S3 Standard-Infrequent Access (IA)
  - suitable for data that is less frequently accessed but requires rapid access when needed
  - high durability 99.9% availability
  - low cost compared to S3 Standard
  - sustain 2 concurrent facility failure
  - disaster recovery, backups etc 
  
- Amazon S3 One Zone Infrequent Access 
  - same as Infrequent access in terms of durability and availability but only available in one AZ
  - data lost when AZ is destroyed
  - low cost (by 20%)
  - secondary backup, or to store data that you can recreate (thumbnail from image)

- Amazon S3 Intelligent Tiering
  - Same low latency and throughput of S3 Standard
  - small monthly monitoring and auto tiering fee
  - automatically moves objects between two access tiers based on changing access patterns
  - designed for durability across multiple availability zones
  - resilient against events that impact and entire availability zones
  - designed for 99.9% availability over a given year
 
- Amazon Glacier
  - low cost object storage for archiving/backup
  - data is retained for longer term (10s of years)
  - alternative to on premise magnetic tape storage
  - average annual durability is 99.999999999%
  - cost per storage month is very cheap
  - each item in glacier is called archive (up t0 40TB)
  - archives are stored in vaults
  
  **3 retrieval options:**
  - Expedited (1 to 5 minutes)
  - Standard (3 to 5 hours)
  - Bulk (5 to 12 hours)
  - Minimum storage duration of 90 days
  
- Amazon Glacier Deep Archive
  - Standard (12 hours)
  - Bulk (48 hours)
  - Minimum storage duration of 180 days 
