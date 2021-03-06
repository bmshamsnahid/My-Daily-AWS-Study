## Flow Logs

- Capture `IP Traffic` and `Network` information
- Help monitor and troubleshoot connectivity issues
  - Can be used for
  - `VPC` level
  - `Subnet` Level
  - `Elastic Network Interface` level
- Store logs in `S3` / `Cloudwatch Logs`
- Can query the logs using
  - `Athena` in `S3` logs
  - `Cloudwatch Log Insights` in `Cloudwatch Logs`
- Can not enable `Flow Logs` of `VPC` that is Peered and belongs to `Another Account`
- After creating a flow log, configuration can not be changed
  - For example, can not change `IAM Roles`
- Following `IP Traffic` does not monitor
  - AWS DNS server
  - Traffic of `Windows Instance` activating licence
  - Traffic of `Instance Metadata` (169.254.169.254)
  - DHCP traffic
  - `Reserved IP Address` of `Default VPC Router`
