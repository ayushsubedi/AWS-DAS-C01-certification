# AWS-DAS-C01-certification
## (WIP) Notes on AWS Data Analytics Speciality Certification

https://aws.amazon.com/certification/certified-data-analytics-specialty

| Topic                                 | %  |
| ------------------------------------- | -- |
| Domain 1: Collection                  | 18 |
| Domain 2: Storage and Data Management | 22 |
| Domain 3: Processing                  | 24 |
| Domain 4: Analysis and Visualization  | 18 |
| Domain 5: Security                    | 18 |


### Domain 1: Collection
1. Determine the operational characteristics of the collection system
2. Select a collection system that handles the frequency, volume, and source of data
3. Select a collection system that addresses the key properties of data, such as order, format, and compression

- [ ] Amazon Kinesis
- [ ] AWS IoT Core
- [ ] AWS Snowball
- [ ] Amazon SQS
- [ ] Amazon DMS
- [ ] AWS Direct Connect

### Domain 2: Storage and Data Management
1. Determine the operational characteristics of a storage solution for analytics
2. Determine data access and retrieval patterns
3. Select an appropriate data layout, schema, structure, and format
4. Define a data lifecycle based on usage patterns and business requirements
5. Determine an appropriate system for cataloging data and managing metadata

- [x] S3
- [x] Glacier
- [ ] DynamoDB
- [ ] ElastiCache 

### Domain 3: Processing
1. Determine appropriate data processing solution requirements
2. Design a solution for transforming and preparing data for analysis
3. Automate and operationalize a data processing solution

- [ ] AWS Lambda
- [ ] Amazon ML
- [ ] Amazon SageMaker
- [ ] Amazon EMR
- [ ] AWS Data Pipeline
- [ ] AWS Glue

### Domain 4: Analysis and Visualization
1. Determine the operational characteristics of an analysis and visualization solution
2. Select the appropriate data analysis solution for a given scenario
3. Select the appropriate data visualization solution for a given scenario

- [ ] Elasticsearch
- [ ] Amazon Athena
- [ ] Amazon Redshift
- [x] Amazon Quicksight

### Domain 5: Security
1. Select appropriate authentication and authorization mechanisms
2. Apply data protection and encryption techniques
3. Apply data governance and compliance controls

- [ ] Amazon KMS
- [ ] AWS CloudHSM

### Courses
- [x] [Data Analytics Fundamentals offered by AWS](https://www.aws.training/Details/eLearning?id=35364) -> [My Notes](https://github.com/ayushsubedi/AWS-DAS-C01-certification/tree/main/aws_data_analysis_fundamentals)
- [ ] [Exam Readiness: AWS Certified Data Analytics - Specialty](https://www.aws.training/Details/eLearning?id=46612)
- [ ] [Udemy course-AWS Certified Data Analytics Specialty 2021 - Hands On!](https://www.udemy.com/course/aws-data-analytics/)
- [ ] [AWS Ramp up Guide-Data Analytics](https://d1.awsstatic.com/training-and-certification/ramp-up_guides/Ramp-Up_Guide_Data_Analytics.pdf)

## Resources

- [ ] [Official Docs](https://docs.aws.amazon.com/)
- [ ] [AWS Certified Data Analytics Specialty 2021 – Hands-On!](https://learning.oreilly.com/videos/aws-certified-data/9781838983383/)
- [ ] [Linux Academy Repo](https://github.com/ayushsubedi/Content-AWS-Certified-Data-Analytics---Speciality)
- [ ] [Sagemaker Immersion Day](https://sagemaker-immersionday.workshop.aws/en/) 
- [ ] [Unofficial Guide](https://awsmaniac.com/the-unofficial-guide-to-aws-certified-data-analytics-specialty-exam/)
- [ ] [Practice exams](https://www.whizlabs.com/aws-certified-data-analytics-specialty/practice-tests/)
- [ ] [Amazon Athena](https://aws.amazon.com/athena/faqs/)
- [ ] [Amazon EMR](https://aws.amazon.com/emr/faqs/)
- [ ] [Amazon Redshift](https://aws.amazon.com/redshift/faqs/)
- [ ] [Amazon Kinesis Data Streams](https://aws.amazon.com/kinesis/data-streams/faqs/)
- [ ] [Amazon Kinesis Data Firehose](https://aws.amazon.com/kinesis/data-firehose/faqs/)
- [ ] [Amazon Kinesis Data Analytics](https://aws.amazon.com/kinesis/data-analytics/faqs/)
- [ ] [Amazon ElasticSearch Service](https://aws.amazon.com/elasticsearch-service/faqs/)
- [ ] [Amazon Managed Service for Kafka (MSK)](https://aws.amazon.com/msk/faqs/)
- [x] [Amazon QuickSight](https://aws.amazon.com/quicksight/resources/faqs/)
- [ ] [AWS Data Exchange](https://aws.amazon.com/data-exchange/faqs/)
- [ ] [AWS Glue](https://aws.amazon.com/glue/faqs/)
- [ ] [AWS Lake Formation](https://aws.amazon.com/lake-formation/faqs/)
- [ ] [Optimize memory management in AWS Glue](https://aws.amazon.com/blogs/big-data/optimize-memory-management-in-aws-glue/).
- [ ] [Process data with varying data ingestion frequencies using AWS Glue job bookmarks](https://aws.amazon.com/blogs/big-data/process-data-with-varying-data-ingestion-frequencies-using-aws-glue-job-bookmarks)
- [ ] [Amazon Redshift Engineering's Advanced Table Design Playbook: Preamble, Prerequisites, and Prioritization](https://aws.amazon.com/blogs/big-data/amazon-redshift-engineerings-advanced-table-design-playbook-preamble-prerequisites-and-prioritization/)
- [ ] [Top 10 performance tuning techniques for Amazon Redshift](https://aws.amazon.com/blogs/big-data/top-10-performance-tuning-techniques-for-amazon-redshift)
- [ ] [Best Practices for Amazon Redshift Spectrum](https://aws.amazon.com/blogs/big-data/10-best-practices-for-amazon-redshift-spectrum)
- [ ] [AWS Well-Architected Framework - Analytics Lens](https://d1.awsstatic.com/whitepapers/architecture/wellarchitected-Analytics-Lens.pdf).
- [ ] [Streaming Data Solutions on AWS with Amazon Kinesis](https://d1.awsstatic.com/whitepapers/whitepaper-streaming-data-solutions-on-aws-with-amazon-kinesis.pdf)
- [ ] [Sizing Cloud Data Warehouses](https://d1.awsstatic.com/whitepapers/Size-Cloud-Data-Warehouse-on-AWS.pdf)
- [ ] [Amazon Redshift: Cost Optimization](https://d1.awsstatic.com/whitepapers/amazon-redshift-cost-optimization.pdf)
- [ ] [Cost Modeling Data Lakes for Beginners](https://d1.awsstatic.com/whitepapers/cost-modeling-data-lakes.pdf)
- [ ] [Migrating to Apache HBase on Amazon S3 on Amazon EMR](https://d1.awsstatic.com/whitepapers/Migrating_to_Apache_Hbase_on_Amazon_S3_on_Amazon_EMR.pdf)
- [ ] [Comparing the Use of Amazon DynamoDB and Apache HBase for NoSQL](https://d1.awsstatic.com/whitepapers/AWS_Comparing_the_Use_of_DynamoDB_and_HBase_for_NoSQL.pdf)
- [ ] [Big Data Analytics Options on AWS](https://d1.awsstatic.com/whitepapers/Big_Data_Analytics_Options_on_AWS.pdf)
- [ ] [Use Amazon Elasticsearch Service to Log and Monitor (Almost) Everything](https://d1.awsstatic.com/whitepapers/whitepaper-use-amazon-elasticsearch-to-log-and-monitor-almost-everything.pdf)
- [ ] [Lambda Architecture for Batch and Stream Processing](https://d1.awsstatic.com/whitepapers/lambda-architecure-on-for-batch-aws.pdf)
- [ ] [Youtube Playlist](https://www.youtube.com/watch?v=TAkcRD6OxPw&list=PLCRlJJDoP5o91Gaj9yq2HIw2CTofIQ4TY)
- [ ] [AWS Analytics Services Cheat Sheet](https://jayendrapatil.com/aws-certification-analytics-services-cheat-sheet/)
- [ ] [Practice Exam](https://www.braincert.com/course/26478-AWS-Certified-Data-Analytics-Specialty-Practice-Exams)

-------------


## Logistics
You are given 170 minutes to complete the exam. It consists of around 65 questions.


## Types and characteristics of exam questions

There are two types of questions on the exam:

- Multiple choice: Has one correct response and three incorrect responses (distractors).
- Multiple response: Has two or more correct responses out of five or more options. These types of questions will explicitly tell you to "(Select TWO)" or "(Select THREE)."

## Use these strategies when answering questions:

- Read and understand the question before reading answer options (pretend the answer options aren't even there at first).
- Identify the key phrases and qualifiers in the question.
- Try to answer the question before even looking at the answer choices, then see if any of those answer choices match your original answer.
- Eliminate answer options based on what you know about the question, including the key phrases and qualifiers you highlighted earlier.
- If you still don't know the answer, consider flagging the question and moving on to easier questions. But remember to answer all questions before the time is up on the exam, as there are no penalties for guessing.
