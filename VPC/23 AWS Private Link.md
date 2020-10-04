## AWS Private Link

- Also known as `VPC Endpoint Service`
- Ideal when, a `Service` needs to be exposed from a `VPC` to multiple `VPC`
- Problem Scenario
  - In my `VPC`, I have a `Web service`
  - Need to expose that service to other `VPC`
  - Possible solution be
    - Make `Web Service` Public
      - This is a security hazard
    - Use `VPC` peering
      - Need to update route table
      - Other services will be accessible as well
- To establish `Private Link`
  - Create a `Network Load Balance` in `Service VPC`
  - Create a `ENI` in the `Customer VPC`
  - Connect `NLB` with `ENI` using the `AWS Private Link`
  - To make it scalable
    - Launch `NLB` in `multi-AZ`
    - Create `ENI` in `multi-AZ`