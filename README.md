### ssmconnect
* This utility was created to connect to EC2 bastion host launched in private subnet without a need to assign public IP, setup SSH keys, etc.
* It generates SSH key pair on the fly and add the public key to bastion host
* It uses Session Manager to connect to bastion hosts that you can launch in private subnets, providing more secure access.
* You can use this utility to login to bastion host OR create a tunnel for RDS or Redshift instances.

**Usage**
```
./ssmconnect -h                 
ssmconnect is a utility to connect to private resources in a VPC using SSM tunnel

Syntax: ssmconnect [-u|i|s|H|l|r|h]
options:
u     OS username of remote instance.
i     EC2 instance id.
s     AWS service name. valid values are ec2, rds and redshift. Default is ec2
l     Local port number if service is rds or redshift.
r     Remote port number if service is rds or redshift.
H     Remote hostname if service is rds or redshift.
h     Print help.
```
