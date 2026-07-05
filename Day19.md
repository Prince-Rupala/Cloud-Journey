# Day 19


## What is Docker?

A software tool that lets you package an application and all its dependencies into a single unit so it runs perfectly on any computer, whether its your laptop or a cloud server.


## What is a container?

A lightweight, isolated, live box running on your computer that holds your application. Think of it like a standard shipping container on a cargo ship: it keeps everything inside isolated from the outside world.


## What is an image?

The unchangeable template or blueprint used to build a container. If an image is a recipe or blueprint of a house, the container is the actual physical house you built from it.


## Difference between VM and container?

Virtual Machine(VM): Packs an entire guest operating system (like Windows or Ubuntu) along with the app. They are heavy, slow to boot, and take gigabytes of spaces.

Container: Shares your computer's existing operating system kernel instead of installing a new one. They are tiny, incredibly fast, and spin up in milliseconds.


## What does docker run hello-world do?

It tests your Docker setup. It downloads a tiny "hello-world" image from the internet, builds a container from it, executes a print command to output a welcome message to your terminal, and then instantly stops.


## What does docker ps -a show?

It lists all containers on your system.

 : docker ps only shows currently running containers.

 : The -a flag stands for "all," showing you containers that are currently running plus containers that have exited or stopped. 
