# Day 27


## Why can't one container use localhost to connect to another container?

Suppose there are two container; backend and database. Now, we want to connect the backend to database, so if we write localhost inside backend container, it wont work, beacuse using localhost means the backend container itself and not database.


## What network does docker compose automatically create?

It will automatically make a your project network like "project"_default. All the services you defined inside the docker-compose.yml are automatically placed inside this network.


## How do container find each other in docker compose?

Container find each other in docker compose over a shared network. Docker includes an internal DNS service. SO when a container asks for : "database", docker's internal DNS resolves it to the correct container IP.


## Why is using service names better than using ip addresses?

Service names are easier for us to remember. Also, services get different ip each time we stop and start containers resulting in disconnect, so if we use service name, docker will automatically fetch their ip and let us stay connected.


## If your service is named: "backend:" what hostname would another container use to connect to it?

The answer is simple "backend" 
