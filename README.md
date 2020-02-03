[![danomisik](https://circleci.com/gh/danomisik/ml-microservice-kubernetes.svg?style=svg)](https://circleci.com/gh/danomisik/ml-microservice-kubernetes)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl


VI editor
:set list - ukaze konce riadkov. Mali by mat iba znak $ (new line)
set ff=unix - nastavuje UNIX konce riadkov

Konvertuj dos subor do unix subor (upravi konce riadkov)

### Solved errors in code
1. I had problem windows end of line in bash scripts. So I changed this end of line to unix supported format:
`tr -d '\15\32' < winfile.txt > unixfile.txt`
2. I had problem to build app.py properly, so I downgrade sklearn
`scikit-learn==0.20.2`


https://computingforgeeks.com/how-to-install-minikube-on-ubuntu-18-04/
https://classroom.udacity.com/nanodegrees/nd9991/parts/652b780f-0423-44bb-a7fa-344325b735e1/modules/67fa9db7-42f2-4e6c-a24a-8ae560da4335/lessons/1597126d-6bef-475c-b248-fead1154776a/concepts/3d8293f6-660d-4cf3-ae10-2067364e596b


kubectl delete deployment ml-service-kubectl
kubectl delete svc ml-service-kubectl


