# Day 38


## What is a Network ACL (NACL)?

NACL stands for Network Access Control List. It provides a protection at subnet level by filtering the outbound and inbound traffic. NACLs are stateless meaning they evaluate traffic independently in each direction.


## What is the difference between a Security Group and a NACL?

Security Group:
1. Security Groups are stateful.
2. Denied unless explicitly allowed is the default behaviour.
3. It works at instance level.
4. Its main purpose is instance-level firewall.

NACL:
1. NACLs are stateless.
2. The default NACL allows traffic by default, while a custom NACL initially denies traffic until rules are added.
3. It operates at subnet level.
4. Its main purpose is to filter traffic at subnet level.


## What does it mean that security groups are stateful?

Suppose EC2 sends something to the internet and receives a response. Now that response is automatically allowed as a part of the previous connection. You don't need to create a inbound rule for that response.


## What does it mean that NACLs are stateless?

Suppose EC2 sends something to the internet, now you need to explicitly allow the return traffic in the inbound rules. It happens because NACLs treat traffic independently in each direction.


## Can a NACL explicitly deny traffic?

Yes, NACL can explicitly deny traffic, in fact it is necessary to do it becausea default NACL allows traffic by default, so you have explicitly allow and deny traffic. Note: The default NACL allows traffic by default, while a custom NACL initially denies traffic until rules are added.


## Can a security group explicitly deny traffic?

No, Security groups can't explicitly deny traffic because it follows allow only rule meaning everything is denied by default unless explicitly allowed.


## Why would a company use both seurity groups and NACLs?

Company usually use security group to act as firewall for EC2 instances, now if company wants an additional layer of protection, they use NACL which filters the traffic at subnet layer.
