# Day 45


## What problem does a Docker registry solve?

Github actions creates the image on the github hosted runner and then execute the "docker run", but github-hosted runner is temporary and closes when the workflow is finished along with our image, so we push the same image to docker registry and can retrieve it to AWS because we dont want to create a new image from dockerfile as there exists the image which passed the tests and works perfectly on our CI.


## Why doesn't the Docker image we build on a GitHub Actions runner automatically become available on AWS?

GitHub actions runner is a temporary. When our workflow finishes running, the runner will be closed completely and also there is currently no known way for AWS to access the github hosted runner for image, so it is ideal to push the image to the registry and AWS pulls it from registry.


## What is Docker Hub?

Docker hub is hosted by docker and is mainly used for image registry.


## What is the difference between docker push and docker pull?

Docker push uploads the image to the registry and docker pull downloads the image from the registry.


## What is a Docker image tag?

Docker image tag is used to tag an image for specific version, like my-app:1.0, my-app:2.0, etc. so finding the specific version of a image is easier.


## Why is versioning Docker images useful?

Versioning makes it easier to find the specific version of the image and helps team to know that a specific version runs flawlessly so they can always rollback to that version if newer version got error or something.


## Why is myapp:1.0 generally more traceable than simply using myapp:latest ?

Because every time someone built a new image and pushed it the latest tag moves to that image so tagging your image with specific pattern like 1.0, 2.0, 3.0, etc is more traceable.


## What does "build once, deploy the same artifact" mean?

It means that if an image is built and passed all the tests then it is more efficient to use that same image rather creating new image everytime.


## What is Amazon ECR?

Amazon Elastic Container Registry is AWS managed container registry service.


## What is the difference between a Docker registry and a Docker container?

Docker registry is like a storage outside your local system where you can push or pull images.

Docker Container is a running instance of a docker image. It is a isolated process for executing your application.
