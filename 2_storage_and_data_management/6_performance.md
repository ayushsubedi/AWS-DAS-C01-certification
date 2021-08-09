# S3 Performance

- Amazon S3 automatically scales to high request rates, latency 100-200ms
- 35000 put/copy/post/delete and 5500 get/head requests per second per prefix in a bucket
- there are no limit to the number of prefix in a bucket

## KMS limitation
- if you use sse-kms, you may be impacted by kms limits
- when you upload, it calls the generatedatakey kms api
- when you download, it calls the decrypt kms api
- count towards the kms quota per second
- you can request increase

## Performance optimization
- multi-part upload
  - recommended for files > 100 mb
  - must use for files > 5gb
  - can help parallelize uploads (speeds up transfers)
- S3 transfer acceleration
  - increase transfer speed by transferring file to an AWS edge location which will forward the data to S3 bucket in the target regions
  - compatible with multip part upload
- S3 byte-range fetches
  - parallelize gets by requesting specif byte ranges
  - better resilience in case of failures
  - can be used to speed up downloads
  - requests can be made in parallel
  - can be used to retrive only partial data
    
