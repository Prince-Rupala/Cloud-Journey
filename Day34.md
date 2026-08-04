# Day 34


## What problem does a NAT gateway solve?

If private servers needs the internet access to download latest software and you typed: sudo apt update, but it will fail because my private server is inside private subnet and there is no route to the Internet Gateway. But if we directly connects to the internet gateway, there is a risk that someone will try to ssh into private server, and there comes the NAT Gateway, it sits in the public subnet and fetchs the response from the internet for the private server without allowing inbound traffic.


## Why can't a private EC2 use the internet gateway directly?

If a private EC2 use the internet gateway directly, there is a risk that someone will try to ssh into it, So to prevent this, we use NAT Gateway, it only allows outbound traffic and gets the requested response and deliver to the private EC2 server without allowing inbound traffic from entering.


## Why is a NAT Gateway placed in a public subnet?

Because NAT Gateway itself needs a route to the internet gateway to carry out its tasks and it can't reach the internet gateway if it is placed inside private subnet as there exist no route to the internet gateway.


## Can someone on the internet SSH into a private EC2 through NAT Gateway? Why?

No, they can't SSH into a private EC2 through a NAT gateway even if they have the private key, because NAT Gateway does not allow inbound traffic, it only allows the reponses requested by private EC2 via NAT Gateway.


## Difference between an Internet Gateway and a NAT Gateway.

Internet Gateway
1. It is used by Public subnets.
2. It allows direct access to the internet.
3. Internet can initiate connections.
4. Mainly used for public servers like Frontend EC2.

NAT Gateway
1. It is used by private subnets.
2. It only allows outbound traffic to the internet.
3. Internet cannot initiate connections.
4. It is mainly used for private servers like Backend EC2.


## Give two examples of when a private EC2 would need outbound internet access.

1. For software updates or new software installation.
2. To connect to external services, if i built a shopping website, it needs a payment services like Razorpay, so to connect to those services.
3. Download Docker Images from the doker hub if they are not already available on the EC2 instances.
