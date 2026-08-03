# Day 32


## What is a VPC?

VPC stands for Virtual Private Cloud. Its like a private isolated network inside the AWS. Inside VPC, we can have our EC2, Database, load balancer, and many other AWS service.


## Why does AWS give every customer a seperate VPC?

Because if AWS does not give every customer a seperate VPC, Company A EC2, Company B Database, Company C Backend would all exist together over a single network, which would create a security disaster. So, AWS gives every customer a seperate VPC so nobody can directly access another customer's VPC and to improve security.


## What is a subnet?

A subnet is a smaller network inside VPC, it is classified into two subnets: Public subnet and Private subnet. A public subnet is used for the services that users should reach. Whereas, private subnet is used for services that should not be directly accessed by the users for security reasons.


## What is the difference between a public subnet and a private subnet?

A public subnet is used for the services that users can reach and directly access like frontend EC2. Whereas, private subnet is used for services that shouldn't be directly accessed by the users like backend EC2 and database EC2.


## Which resources are usually placed in a public subnet?

Resources like Frontend EC2, bastion hosts, load balancers, web servers, etc.


## Which resources are usually placed in a private subnet?

Backend EC2 and Database EC2 are usually placed in a private subnet.
