[![CircleCI](https://circleci.com/gh/gradjitta/mlapp-project.svg?style=svg)](https://circleci.com/gh/gradjitta/mlapp-project)

## Project Overview

In this project, we operationalize a Machine Learning Microservice API. 

We are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. 

### Project Tasks

Project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications.

### Tasks

#### Test your project code using linting
- Testing was done at code level with `pylint` and the dockerfile was tested using `hadolint`
#### Complete a Dockerfile to containerize this application
- [x] Finished a [Dockerfile](https://github.com/gradjitta/mlapp-project/blob/master/Dockerfile)
- [x] Deploy containerized application using Docker and make a prediction
- [x] Improve the log statements in the source code for this application

#### Pushed the container to Docker Hub
```
docker build . -t mlapp-project
docker login
docker tag mlapp-project:latest gradjitta/mlapp:latest
docker push gradjitta/mlapp
```

#### Configure Kubernetes and create a Kubernetes cluster
- [x] Created kubernetes node with minikube and deployed the container
- [x] Deploy a container using `kubectl` and make a prediction. Makes use of the docker hub image.
