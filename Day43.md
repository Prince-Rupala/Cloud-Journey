# Day 43


## What is the purpose of docker build in our CI pipeline?

It builds the custom image from our Dockerfile and then that image is used to make a docker container.


## Where does the Docker image get built when GitHub Actions runs the workflow?

Docker image is built on the machines provided by Github called runner.


## Why do we use docker run after docker build?

Because docker build is used to build the image which is like a blueprint for the container and docker run executes the container which are made from the images. So, if we run docker run before docker build then that container won't execute as there is no image for it.


## What would happen if docker build failed?

The pipeline would stop and will not proceed further if the docker build failed, as some of the next steps needs dockder build to be successful like docker run.


## What would happen if docker build succeeds but docker run fails?

If docker build succeeds, the pipeline will move to the next process which is docker run and if the docker run fails the pipeline will stops and will not proceed to next stage


## Why is it useful to test the docker container inside CI instead of only testing it on the developer's laptop?

Sometimes the docker container runs on the developers laptop as it contains all the dependencies, but may fail on EC2, so it is better to test the docker container inside CI also.


## What is the difference between testing the source code and testing the docker container?

Testing the source code means testing the direct code developers write to check all the functionalities and parameters. Whereas, testing the docker container means packaging the code and all its dependencies in the docker image and testing it by running the container.
