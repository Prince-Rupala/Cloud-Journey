# Day 26


## What problem does Docker Compose solve?

Without Docker Compose i have to run multiple container one-by-one, with docker compose I can run multiple containers together, so i dont need to remember container name, port mapping, volumes, networking, etc. Think Docker Compose like a recipe for many containers.


## What is a service in compose?

A service is the definition of how Docker should create and run a container. It includes settings such as the image, ports, volumes, environment variables, and networks.


## What does docker compose up -d do?

It runs the docker-compose.yml file, executing all the containers in the file.


## What does docker compose down do?

It basically means docker stop ... and docker rm ..., it stops and remove all the containers in compose file.


## Difference between Dockerfile and docker-compose.yml?

Dockerfile: It is like a recipe to make a single image.

Docker-compose.yml: It is like a recipe for many containers.


## Why is compose useful for multi-container application?

You can start or stop an entire stack of containers- whether 2 or 20 with just docker compose up or down. It also frees us from the hassle from running all the container one-by-one.
