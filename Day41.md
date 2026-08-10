# Day 41


## What problem does CI/CD solve?

Without CI/CD, when developers push new code to github, I need to manually SSH into server, pull the changes, build docker images, stop old container and then start a new container. CI/CD  automates much of this entire process once designed properly.


## What does CI stand for?

CI stands for Continuous Integration. A team of developers merges their code into a shared repository and CI checks whether the new code works. If it does not works, the team gets notified before the code gets deployed.


## What does CD stand for?

CD stands for Continuous Delivery or Continuous Deployment. It automatically packages the validated code and makes it ready to go to production at the click of a button; Continuous Deployment even automates the manual intervention and automatically releases the changes to end users.


## What is a CI/CD pipeline?

CI/CD pipeline automates the sequence of process that a code goes through and after successfully going through each processes the code becomes ready for deployment.


## What might happen after a developer runs git push in a CI/CD workflow?

When a developer runs a git push, github receives the code. A CI/CD workflow detects that push and automatically starts the pipeline to make the code validated and ready for the deployment. (Note: Deploys code to the end user in case of Continuous Deployment).


## Why should tests run before deployment?

If the code fails the test, the pipeline should stop because I don't want the broken code reaching to the deployment stage. That's why tests run before deployment.


## How does Docker fit into CI/CD?

CI/CD automates the docker build image, contanerising the app and deploy the container. So, entire docker fit as a part of the CI/CD pipeline.


## What is the difference between Continuous Delivery and Continuous Deployment?

Continuous Delivery: It automatically packages the validated code and make it ready to go to production at the a single click.

Continuous Deployment: It takes delivery one step further by automatically deploying every passing change directly to the end users without any manual intervention.
