# Description
This template deploys a VPC, with a pair of public and private subnets spread across two Availability Zones. It deploys an internet gateway, with a default route on the public subnets. It deploys a pair of NAT gateways (one in each AZ),  and default routes for them in the private subnets. Name tags are created for supported resources including the Environment parameter value.
This template can be deployed with default values to quickly create a VPC in an empty AWS account / region.

# Template Parameters
| Parameter | Description | Mandatory | Default value |
| --- | --- | --- | --- |
| EnvironmentName | An environment name that is prefixed to resource names | yes | defaultvpc |
| VpcCIDR | The IP range (CIDR notation) for this VPC | yes | 10.17.0.0/16 |
| PublicSubnet1CIDR | The IP range (CIDR notation) for the public subnet in the first Availability Zone | yes | 10.17.10.0/22 |
| PublicSubnet2CIDR | The IP range (CIDR notation) for the public subnet in the second Availability Zone | yes | 10.17.20.0/22 |
| PrivateSubnet1CIDR | The IP range (CIDR notation) for the private subnet in the first Availability Zone | yes | 10.17.110.0/22 |
| PrivateSubnet2CIDR | The IP range (CIDR notation) for the private subnet in the second Availability Zone | yes | 10.17.120.0/22 |