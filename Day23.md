# Day 23


## What is port mapping?

It routes the traffic from internet to my local device to docker to app inside the container.


## What does -p 8080:80 mean?

It connects the host port 8080 to container port 80. Any traffic coming on port 8080 will be forwarded to port 80 inside the container.


## Why couldn't you access nginx before port mapping?

Because without port mapping there is way to connect the container as it is isolated network. So to forward the traffic we need to connect the container port to local host port.


## What does -d do?

It stands for detached mode. It runs the container in background so terminal remains free.


## If a container app listens on port 3000 and you run:
   docker run -p 5000:3000 my-app
   which URL would you open in your browser?

I would open http://localhost:5000


## Does changing the host port change the application's internal port?

No, changing the host port does not affect the internal port.
