# Day 36


## What is Amazon S3?

S3 stands Simple Storage Service. It is a service provided by the Amazon for storage. It is a giant cloud storage system to save all the files for the company.


## What is an S3 Bucket?

Think S3 Bucket like a folder, every object goes inside a bucket. Using S3 buckets we can store different files files (objects) in different folder (bucket) like images can be saved in company-images bucket, logs can be saved in company-logs bucket, etc.


## What is an Object in S3?

Think files as a object which gets stored in S3. Each object has a name, data and metadata. Examples of objects: image.png, code.zip, video.mp4, etc.


## Why would a company store images in S3 instead of EC2?

Because EC2 is made for running applications, using S3 for storing a images is highly practicle as it is cheaper, more durable and made specifically for storing files.


## Difference between a public bucket and a private bucket?

Public buckets contains the files which should be accessible by the users such as company logo. Whereas, private buckets contains the files which should notbe directly accessible by the public such as private info of users.


## What problem does Versioning solve?

Imagine i uploaded a file on S3, later i accidently overwrite it, if the versioning is not enabled i lost the olderversion, but if versioning is enabled the newer version is saved as: original-file.pdf, Version 1, Version 2. Now i can restore my older version.


## Summary

EC2 = Compute (Runs applications)

S3 = Object Storage (Stores files)

Bucket = Container

Object = File

Versioning = Protects against accidental overwrite or deletion.
