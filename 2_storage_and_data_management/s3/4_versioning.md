# S3 Versioning

- versioning is possible in S3
- enabled at bucket level
- same key overwrite witll increment the version
- it is considered good to be versioninig your buckets
  - easy to roll back
  - protect against unintended deletes 
- any filed not versioned prior to enabling versioning will have null as its version id
