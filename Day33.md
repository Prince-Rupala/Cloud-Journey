# Day 33


## What is a Route table?

A Route Table is a list of routing rules. It defines the path to the destination. For Example: destination: 10.0.0.0/16 then path: local. It basically tells if the traffic is going to this destination, use this path.


## Why does every subnet need a Route Table?

Every subnets have a Route table beacause a subnet becomes a public subnet or private subnet depending if the subnet's associated route table has a route pointing to the internet gateway or not repectively. Every Route table contains a local path enabling the internal communication using their private IPs. And if the route table has a route pointing to the internet gateway, it makes the subnet a public subnet and if it doesn't have that path it means the subnet is private.


## What does the local route do?

It enables the the internal communication inside the VPC using their Private IPs.


## What makes a subnet public?

If the route table has a path to the internet gateway, then it means that internet can now reach that subnet making it a public subnet.


## What makes a subnet private?

If the route table has no path to the internet gateway means that internet has no reachability to the subnet, making the subnet a private subnet.


## Why isn't having a public IP alone enough for the internet access?

Because even if my EC2 instance has a public IP, it needs to be in public subnet whose associated route table has a route pointing to internet gateway to reach the internet. Even after that there are other things like security groups to take account into.


## Internet Access Requirements:

1. Public IP
2. Public Subnet (Route Table → Internet Gateway)
3. Security Group allows traffic

Missing any one of these → No direct internet access.
