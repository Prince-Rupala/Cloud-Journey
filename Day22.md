# Day 22


## What is a Dockerfile?

A simple text file containing step-by-step instructions that docker uses to build a custom Docker image.


## What does FROM ubuntu do?

It gives the docker instructions to start with Ubuntu image.


## What does RUN do?

It executes commands while building the image.


## What does CMD do?

It tells the docker to run this command when the container starts.


## Difference between docker build and docker run?

Docker build reads the Dockerfile, then created image and lastly stores that image locally.

Docker run uses the image to build a container and execute the cmd command.


## Why would a company use a Dockerfile instead of manually configuring containers?

Anyone on the team can run docker build and get the exact same environment in seconds, eliminating "it works on my machine" issues.
