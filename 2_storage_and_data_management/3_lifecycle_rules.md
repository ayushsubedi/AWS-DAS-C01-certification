# S3 Lifecycle rules

- You can transition objects between storage classes
- Moving objects can be automated using a lifecycle configuration


- Transition actions: It defines when objects are transitioned to another storage class
  - Move objects to Standard IA class 60 days after creation
  - Move to glacier for archiving after 6 months

- Expiration actions: configure objects to expire after some time
  - access log files can be set to delete after 365 days
  - can be used to delete old versions of files (if versioning is enabled)
  - can be used to delete incomplete multi-part uploads

- Rules can be created for a certain prefix (ex - s3://bucket/this/*)
- Rules can be created for a certain tag

____________

## S3 Lifecycle Rules 

### Scenario I

Your application on EC2 creates images thumbnails after profile photos are uploaded to Amazon S3. These thumbnails can be easily recreated, and only need to be kept for 45 days. The source image should be able to be immediately retrieved for these 45 days, and afterwards, the user can wait up to 6 hours. How would you design this?
- S3 source images can be on standard with lifecycle configuration to transition them to glacier after 45 days
- s3 thumbnails can be on onezone_ia with lifecycle configuration to expire them after 45 days

### Scenario II

A rule in your company states that you should be able to recover your deleted S3 objects immediately for 15 days, although this may happen rarely. After this time, and for up to 365 days, deleted objects should be recoverable within 48 hours. 
- S3 versioning
- transition the non-current versions into S3_IA
- transition afterwards to Deep archive
