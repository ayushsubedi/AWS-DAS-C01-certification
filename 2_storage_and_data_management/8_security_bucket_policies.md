# S3 security and bucket policies

- User based
  - IAM policies - which API calls should be allowed for a specific user from IAM console
  
- Resource based
  - bucket policies - bucket wide rules from the S3 console, allows cross account
  - object access control list (ACL) - finer grain
  - bucket access control list (ACL) - less common

-----

- an IAM principal can access and S3 object if
  - the user IAM permissions allow it or resource policy allows it
  - and there is no explicit deny

- JSON based policies
  -  resources: buckets and objects
  -  actions: set of api to allow or deny
  -  effect: allow or deny
  -  principal: the account or user to apply the policy to

- S3 bucket policy to:
  - grant public access to the bucket
  - force objects to be encrypted at upload
  - grant access to another account (cross account)

- Bucket setting for block public access
  - Block public access to buckets and objects granted through
    - new access control lists
    - any access control lists
    - new public bucket or access point policies
  - These settings were created to prevent company data leaks
  - If you know your buckets should not be public, leave these settings on.   
 
