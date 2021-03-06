## S3 Replication

- `S3` allows
  - CRR (Cross-region-replication)
    - Use for
      - compliance
      - Lower latency access
      - Replication across accounts
  - SRR (Same-region-replication)
    - Use for
      - Log aggregation (centralized multiple log buckets data)
      - Replication between production, test and staging accounts
- Can be replicated to a `Bucket` of another account
- Replication is asynchronous
- To enable `replication`
  - Versioning must be enabled in both
    - Source Bucket
    - Destination Bucket
  - Should have an proper `IAM Policy`
- Activating `Replication` does not replicate the existing objects
- `Delete` operation does not replicate
- No `Chaining Replication` happen
  - `Bucket 1` replicate to `Bucket 2`
  - `Bucket 2` replicate to `Bucket 3`
  - This does not imply `Bucket 1` replicate to `Bucket 3`
