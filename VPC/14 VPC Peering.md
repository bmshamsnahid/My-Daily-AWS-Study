## VPC Peering

- Connect two `VPC` using AWS network
- After `VPC Peering` communication between two `VPC` use `AWS Network` instead of `Public Internet`
- Two `VPC` should not have overlapping `CIDR`
- A `Peered Connection` is to be created between two `VPC`
- `Peered Connection` can be established with an `VPC` in another `Region` and another `Account` (`inter-region`, `cross-account`)
- Can use `Peered VPC SG` reference
- Connection is not `Transitive`
  - `VPC A` is peered to `VPC B`
  - `VPC B` is peered to `VPC C`
  - Does not imply `VPC A` is peered with `VPC C`
  - Still we need to peer `VPC A` with `VPC C` explicitly
- Each `Subnet Route Table` of each peered `VPC` should be updated.
  - Target of the `Peered VPC CIDR` should be the `Peered Connection`
- To establish `VPC Peering`
  - Create `VPC Peer Connection` with own `VPC` and another `VPC`
  - Accept the `Peer Connection` request
  - Update `Subnet Route Table` for both `VPC`