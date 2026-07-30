# Day 29


## What is EC2?

EC2 stands for Elastic Compute Cloud. It is a service provided by AWS where one can launch and manage virtual machines in AWS.


## Why would a company use EC2 instead of running application on an employee's laptop?

If a company uses their employee's laptop for running then when that employee turns off their internet and laptop to check-out for the day, the app will also goes down. Using EC2 solves that problem, so even after that employeeshut down their system, the app will be up and available for the users.


## What is an AMI?

Before creating EC2 instance, AWS asks for operating system for instance, this choice comes from Amazon Machine Image (AMI). Think AMI like a ready-made template for our virtual machine.


## What is an instance type?

Instance type in AWS is means different combinations of the hardware, you select the one which fulfills your requirement.


## Why are key pairs used instead of passwords?

Key pairs are far more superior than passwords in terms of protection, beacause passwords can be cracked using automated bot but it is virtually immpossible to crack the keys. Public-key cryptography is much more secure than password authentication because the private key never leaves your computer.


## What is the purpose of the security group?

Security group is like firewall for Virtual machine, its main purpose is to protect the VMs from unknown traffic.
