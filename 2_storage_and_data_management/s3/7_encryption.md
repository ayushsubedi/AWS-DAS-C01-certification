# S3 encryption

There are four methods of encrypting objects in S3
- SSE-S3: encrypts S3 objects using keys handled and managed by AWS
- SSE-KMS: AWS Key Management Service to manage encryption keys
- SSE-C: when you want to manage your own encryption keys
- Client Side Encryption

### SSE-S3 
- server side encryption
- keys handled and managed by AWS
- AES-256
- Must set header: "x-amz-server-side-encryption":"AES256"

### SSE-KMS
- server side encryption
- control over who has access to keys and audit trail
- header: "x-amz-server-side-encryption":"aws:kms"

### SSE-C
- server side encryption using data keys fully managed by the customer outside of AWS
- S3 does not store the encryption key you provide (and must provide)
- HTTPS must be used (because keys are being passed)
- Encryption key must be provided in HTTP headers, for every HTTP request made
- more management on customer's end

### Client side encryption
- client encrypts before sending it to S3
- clients decrypts when retrieving from S3
