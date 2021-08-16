# S3 overview

- Amazon S3 allows people to store objects (files) in "buckets"
- Buckets must have a globally unique name
- Defined at the region level
- Naming convention
  - no uppercase
  - no underscore
  - 3-63 characters long
  - cannot be an IP
  - must start with letter or number (letter needs to be lowercase)

The following example bucket names are valid and follow the recommended naming guidelines:

-   `docexamplebucket1`

-   `log-delivery-march-2020`

-   `my-hosted-content`

The following example bucket names are valid but not recommended for uses other than static website hosting:

-   `docexamplewebsite.com`

-   `www.docexamplewebsite.com`

-   `my.example.s3.bucket`

The following example bucket names are *not* valid:

-   `doc_example_bucket` (contains underscores)

-   `DocExampleBucket` (contains uppercase letters)

-   `doc-example-bucket-` (ends with a hyphen)


- Objects (files) have a key. The key is the full path:
  - <bucket>/my_file.txt
  - <bucket>/first_folder/second_folder/my_file.txt
- There is no concept of directories within buckets. 
- These are just keys with very long names that contain the "/"
- The values are the content of the body with max size of the file being 5GB (but multi part upload is supported for more than 5 GB)
  - There are advantages of using multipart uploads for file size much smaller though
- Metadata
   - list of text key/value pair -system or user metadata
- tags (unicode key/value pair - up to 10) and useful for security and lifecycle
- version ID (if versioning is enabled)
  
  
  
 # Consistency
 - After December 2020, any subsequent read or list request refers to the latest S3 bucket (after put or delete)
