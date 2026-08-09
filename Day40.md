# Day 40


## What problem does Auto Scaling solve?

Suppose I have made a e-commerce app, now i run it in two EC2 instance to handle the regular traffic, during sale the traffic increases so i have to increase the EC2 instance manually and when the traffic decreases after sale ends, i have to decrease the EC2 instances manually again which is not practicle. Now, Auot scaling does this automatically solving the problem. It automatically adjusts the number of EC2 instances based on demand and predefined rules.


## What is scaling out?

Scaling out means adding more EC2 instances. Companies do this to handle more traffic when the demand increases.


## What is scaling in?

Scaling in means removing EC2 instances when they are not needed. This helps in cutting unneccessary cost.


## What is the difference between vertical scaling and horizontal scaling?

Vertical scaling: In Vertical scaling you make one server bigger by adding more CPU/RAM.

Horizontal scaling: In Horizontal Scaling you add more smaller servers instead of the one large server.

In cloud application, horizontal scaling is extremely useful because it improves both capacity and availability, whereas vertical scaling only improves capacity.


## What is the relationship between auto scaling and a load balancer?

Auto scaling and load balancer works together to improve scalability and availability. Auto scaling decides to increase or decrease the number of the server required based on demand and predefined rules. Whereas, Load balancer distributes the traffic between healthy servers.


## Give two examples of metrics that could trigger Auto Scaling.

1. CPU utilization: If CPU > 70% then launch another EC2 and If CPU < 30% then remove an unneccessary EC2.
2. Request count: If the traffic increases and cross a certain threshold then launch another EC2.


## What do minimum, desired and maximum capacity mean?

Minimum Capacity: The minimum number of server i want, this maintain at least 2 instances.

Desired Capacity: The normal number of instances, usually set at the number of instances i want to handle regular traffic.

Maximum Capacity: The maximum number of instances allowed, meaning even during high traffic, it won't go beyond the maximum capacity.


## What happens if an EC2 instance managed by Auto Scaling becomes unhealthy?

Auto Scaling can detect that a particular instance has become unhealthy and launch a replacement, so the returned to the desired capacity.
