## KMS

- When key is managed by in house security team'
  - For Encryption
    - Generate data key using Customer managed Cmk
    - Encrypt data with data key
    - Delete data key
    - Store encrypted data key and data in S3
  - For decryption
    - Use CMK to decrypt data key
    - Decrypt data using `Decrypted data key`
- `KMS Master Key` is region specific

### Envelope Encryption

- `CMK` is used to `generate`, `encrypt` and `decrypt` the `data keys`
- `Data Keys` are used to `encrypt` and `decrypt` the data, from outside the `AWS`
