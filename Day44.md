# Day 44


## What is an automated test?

Automated test checks the application code automatically to verify whether the code works or jot and only if the test pass the CI pipeline moves to next stage and if the test fails the CI pipeline would not proceed further


## Why should tests run before deployment?

Because we don't want the broken code to reach the deployment stage so the tests run before deployment.


## What is a unit test?

A unit test tests small individual piece of code. We are not testing the entire website but just small piece of functionality.


## What is pytest?

Pytest is a testing framework which tests the code so we don't have to manually run every test.


## What does actions/setup-python do?

It sets up the specified Python environment/version on the github actions runner.


## Why do we install pytest inside the github actions runner?

We install pytest because the Github Actions runner is a fresh environment and doesn't automatically have the testing framework our project needs.


## What happens to the pipeline if pytest fails?

If the pytest fails the pipeline stops immediately and won't go to build docker image stage as we don't want to the broken code to reach the deployment stage.


## Why is the test stage placed before docker build?

By placing the test stage placed before docker build the pipeline wont proceed further if the test fail, we want this because we don't want to waste resources to build image and run container of the broken code which would be complete waste.


## What does working-directory do?

This tells github actions to go to the specific directory and do actions their, for example: Pytest: This runs pytest in that specific directory.


## What is the difference between testing your python code and running the docker container? 


Testing the python means testing the application functions, logic, etc

Running the docker container means executing the container which is build from the image which is build from the application code. It basically means packing your application in image and building the doker container from it so app runs in isolated environment.
