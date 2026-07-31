# Day 31


## What is a private IP?

Private IP is used for internal communication in AWS like frontend EC2 to backend EC2 or backend EC2 to database EC2. This is faster, cheaper and more secure. AWS automatically gives the EC2 private IP.


## What is a public IP?

If i want users to reach my website, the traffic cant reach because private IP is not routable over the internet. Therefore, AWS assigns public IP to your EC2, now anyone can reach your server.


## Why does an EC2 instance often have both?

Because private IP supports internal communication between backend, database and frontend as database and backend cant be exposed on public IP. Whereas, public IP is needed so the users can reach your server.


## What is an internet gateway?

Internet Gateway is like a path that connects internet to your EC2 public IP, without internet gateway, internet cant connect to you EC2 even though you have a public IP.


## Why don't database usually have public IP addresses?

Because if database has a Public IP, users can directly access your database which consists of users data and sensitive information.


## Which server normally have public IPs?

Normally only frontend has a public IP as the main purpose of the frontend is to be accessed by a user directly. Backend and Database should never have a public IPs as they have the information which should not be accessed by the users.
