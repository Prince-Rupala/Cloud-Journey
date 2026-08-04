# Day 35


## What is IAM?

IAM stands for Identity and Access Management. It basically controls who can log in, what they can access, and what actions they can perform. It only gives the specific access and permissions to the necessary individual or group.


## Why shouldn't we use the root user for daily work?

The Root user has unlimited permissions, can delete the AWS account, can delete everything, making the use of this account for daily work highly impractical due to the risk of accidental deletion.


## What is an IAM user?

IAM user is the individual who gets the usernme and password for establishing their own identity and this identity gets specific access and permissions for the specific resources for their work.


## What is an IAM Group?

Imagine a team of developers are working together on backend, now if we assign each person backend access and permission one-by-one, the process gets lengthy, so we make the group of all the developers of the team and assign that group an access to the backend and necessary permissions.


## What is an IAM Policy?

Policy states what a specific individual or group are allowed to do. For Example: Developer policy: can launch and stop EC2, cannot Delete VPC and close the AWS account.


# What is the principle of Least Priviledge?

Principle of leats privilegde defined as giving as least as possible permissions to the individual or group to complete their work.


## Summary

Root User
│
├── Full Access
├── Enable MFA
└── Rarely Used

IAM
│
├── Users
├── Groups
└── Policies

Policy = Permissions

Best Practice:
Give only the permissions needed.
