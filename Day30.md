# Day 30


## What is SSH?

SSH stands for Secure Shell. It is a protocol that lets you conneect to another computer safely over a network.


## Why do we use SSH with EC2?

If my EC2 server is in the mumbai region, I cant travel from ahmedabad to mumbai up and down every time i want to use my server, that's why we use SSH with EC2, so can control the server remotely.


## What does this command mean? ssh -i my-key.pem ubuntu@18.204.xxx.xxx. Explain each part.

This command is used for SSH protocol to connect our laptop with our EC2 server. "ssh" means start SSH connection. "-i my-key.pem" means use "my-key.pem" private key. "ubuntu" is a username for ubuntu AMI. "18.204.xxx.xxx" is the public ip address for my EC2 server.


## Why do we run: chmod 400 my-key.pem

Because "my-key.pem" is a private key and if that file have 777 permission, SSH would refuse to use it as it can't go outside of your laptop, for this reason the private key file can only have read only permission and that too only for the owner.


## After connecting through SSH, where do your commands execute?

After connecting through the SSH, all the commands will be executed on the the EC2 server because the terminal is now connected to EC2.


## Why is SSH considered secure?

SSH is considered secure because it encrypts all the communication, it uses key based authentication, and prevents password from being sent over the network.
