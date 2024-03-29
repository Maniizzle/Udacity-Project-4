[![CircleCI](https://dl.circleci.com/status-badge/img/gh/Maniizzle/Udacity-Project-4/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/Maniizzle/Udacity-Project-4/tree/main)
## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

The project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project I will:
* Test the project code using linting
* Complete a Dockerfile to containerize this application
* Deploy a containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---
## Task
Operationalizing a machine learning python microservice with an endpoint that returns a prediction after receiving an input.

### Setup the Environment

* Create a virtual environment by executing:  `python3 -m venv devopsenv`
* Activate it by executing: `source devopsenv/bin/activate`
* Run `make install` to install the necessary dependencies

### Running the application

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./upload_docker.sh && ./run_kubernetes.sh`


## Files

| Folder/File | Description |
| ---- | ----------- |
| `.circleci/config.yml` | CircleCI configuration |
| `model_data` | Trained model data for housing prices in Boston |
| `docker_out.txt` | log output when running the application on docker |
|`kubernetes_out_put`|log output when running the application on kubernetes |
| `app.py` | REST API with an endpoint for predicting housing prices in Boston |
| `Makefile` | Build file of the project |
| `requirements.txt` | Python app dependencies |
| `Dockerfile` | Dockerfile for containerizing the application |
| `run_docker.sh` | Shell script for creating and running docker container |
| `upload_docker.sh` | Shell script for uploading locally built docker image to dockerhub repository |
| `make_prediction.sh` | Shell script to test the running application and returns a prediction |
| `run_kubernetes.sh` | Shell script to deploy docker container on Kubernetes cluster |
