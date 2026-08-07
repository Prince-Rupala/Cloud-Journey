# Day 37


## What is Amazon RDS?

RDS stands for Relational Database Service. Instead of manually installing and managing the database, AWS manages databases for you. Amazon RDS supports many database engines like MySQL, PostgreSQL, MariaDB, Oracle, etc.


## Why would a company use RDS instead of installing MySQL on EC2?

A company can install MySQL on EC2 but then they are responsible for installing it, updating it, backups, monitoring, High availability, Recovering after failures, etc. But with RDS, AWS manages this for you, that's why companies often choose RDS.


## What problem do automated backups solve?

If some new intern accidently deletes the customer data, now if backups was created, the company can restore yesterday's database. But without backups, the data may be permanently lost. RDS automatically creates backups for you.


## What is Multi-AZ deployment?

Multi-AZ deployment means deploying your database in another Availability Zone which remains stand-by and if the primary fails, AWS can automatically switch to the stand-by, so your application keeps working. This improve the overall availability.


## Why are RDS databases usually placed in private subnets?

RDS databases usually placed in private subnets because users should never connect directly to the database as it may contain sensitive user data. Database is usually only accessed by the backend using private ip.


## Give three examples of data that would be stored in an RDS database.

1. User accounts
2. Payment history
3. Orders
