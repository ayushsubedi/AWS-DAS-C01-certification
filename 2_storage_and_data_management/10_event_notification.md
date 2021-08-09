# Event Notification

- S3:ObjectCreated
- S3:ObjectRemoved
- S3:ObjectRestore
- S3:ObjectReplication ...

- Object name filtering is possible
- can create as many s3 events as desired
- typically deliver events in seconds but sometime can take longer
- sometimes one event notification might only be sent if non-versioned object (when write)
- versioning will solve the issue


# Event destinations
- Lambda
- SQS
- SNS

- make sure permissions are set up properly
