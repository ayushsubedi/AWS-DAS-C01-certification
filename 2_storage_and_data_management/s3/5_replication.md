# S3 replication (CRR and SRR)

- Must enable versioning in source and destination
- Cross Region Replication (CRR)
- Same Region Replication (SRR)
- Buckets can be in different accounts
- copying is asynchronous
- must provide proper IAM permissions to S3

### CRR
- compliance, lower latency access, replication across acccounts

### SRR
- log aggregation, live replication between production and test accounts

### Notes
- after activating, only new objects are replicated
- for delete operations:
  - can replicate delete markers from source to target (optional setting)
  - deletions with a version ID are not replicated (to avoid malicious deletes)

- There is not chaining of replication
- If bucket 1 replicated to bucket 2 is replicated to bucket 3, objects created in bucket 1 will only be replicated to bucket 2
