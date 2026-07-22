# Day 24


## What does WORKDIR do?

It does the same function as "mkdir /app \ cd /app". Without WORKDIR "." wouldnt know which directory to work on.


## What does COPY app.py . do?

It copies app.py from my local project directory into the current working directory inside the Docker image.


## Why did we expose port 8000?

So we can connect the port to localhost port for routing incoming traffic.


## Difference between running python3 app.py directly and running it inside docker?

If we run python3 app.py directly we need all its dependencies installed in our local device and if we run it inside the docker, all its dependencies will be packed in the container. Right now we can run directly as well as inside the docker but if someone else need to run this app, they may face difficulty running directly compared to running inside docker as "it works on my computer" issue may arise.


## Why is Docker useful for application?

As I have said in the above question, it eliminates "it works on my machine" issue making it vey useful for application.
