# Day 39


## What problem does a load balancer solve?

If a very large number of users access the frontend EC2 at the same time, one server may become overload or fail, so we use multiple EC2 instances. Now, another problem has arise about how to distribute the traffic between multiple servers and the answer is Load Balancer. Load Balancer receives traffic and distributes it across multiple EC2 instances. This helps in improving scalability.


## Why would a company use multiple EC2 instances instead of one?

If a very large number of users access the EC2 instance at the same time, one server may became overload or fail, so company uses multiple EC2 instances, so traffic gets distributed across multiple EC2 instances.


## What happens if one EC2 instance behind the load balancer fails?

If one EC2 instance behind the load balancer fails, load balancer stops routing the traffic to that EC2 instance and distributes the traffic across healthy EC2 instances. This improves availability of the application.


## What is a health check?

Health check is the process by which load balancer know that a particular server is broken or not. Load balancer might periodically request GET /health, if the server responds correctly that means the server is healthy and if it fails that means the server is unhealthy. The load balancer stops routing traffic to the unhealthy server.


## Why don't users need to know the individual EC2 IP addresses when using a load balancer?

Because users interacts with the load balancer instead of individual EC2 instances. EC2 instances can be added, removes or replaced without requiring users to know their individual IP addresses.


## What is an Elastic Load Balancing (ELB)?

AWS provides a managed load balancing service called Elastic Load Balancing (ELB). You don't have to build your own load-balancing server, instead AWS handles the infrastructure required for the load balancer.


## What is the difference between a Load Balancer and a security Group?

Load balancer distributes the traffic between multiple servers. Whereas, security group allows or denies traffic from entering the EC2 instance.
