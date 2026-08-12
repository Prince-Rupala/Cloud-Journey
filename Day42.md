# Day 42


## What is GitHub Actions?

GitHub is a feature of GitHub that allows you to automate tasks when something happens in the repository.


## What is a workflow?

A workflow is an automated process defined inside your GitHub repository. GitHub Actions workflows are normally stored in: ".github/workflows/". The .yml file stored inside the .github/workflows tells github: "when this happens, perform this steps."


## What is the trigger?

A trigger tells GitHub when to start the workflow. It means run the workflows when something specific happens.

For example:

on:
  pull_request:

This means the workflow can run when someone creates or updates a pull request.


## What is a job?

A job is a collection of steps that GitHub executes when a specific actions triggers the workflows.


## What is a step?

A step is an individual action inside a job such as install python, run tests, etc. so, the hierarchy follows Workflows --> Job --> Steps.


## What is a runner?

Workflow needs a computer to execute the commands and GitHub provides these machine, called runners.

For example: runs-on: ubuntu-latest
this means github runs this job on an Ubuntu runner.


## What does this means?: runs-on: ubuntu-latest

This tells the GitHub to run this job on Ubuntu runner.


## Why do we use actions/checkout@v4?

This downloads or checks your repository's code onto the server. We need to use this because the runner doesn't automatically contain your repository files.


## What is the difference between uses: and run:?

uses: It is used when specific action is needed to be executed such as actions/checkout@v4.

run: It is used to execute the shell command on the runner.


## What happens when you push ci.yml to GitHub?

When the ci.yml file is pushed to GitHub, it tells the GitHub "When code is pushed to main, start the workflow"
