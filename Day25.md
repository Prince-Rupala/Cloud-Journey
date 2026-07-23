# Day 25


## Why is having multiple containers better than one giant container?

Because multiple containers are easier to update or fix without interrupting another containers which has database, Nginx, etc.


## What problem does container seperation solve?

As i have said above, if a specific container fails, it doesnt affect another Containers.


## If only the backend changes, why is a multi-container design helpful?

Because i only have to work on backend container, and database container and frontend container runs without any issues.


## What does it mean when people say "a container should have a single responsibility"?

It means that a single container only focus entirely on doing single task.


## Simple example of three containers working together

Imagine an online shoppingb app:

[User Browser]
      |
      v
1. Frontend Container ---> serves the web page
      |
      v
2. Backend Container ---> Processes payment
      |
      v
3. Database Conatainer ---> Saves orders & user profiles
