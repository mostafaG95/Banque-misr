# Banque-misr

# CI/CD for Spring Boot Application

This repository contains the CI/CD pipeline setup for a Spring Boot application using Jenkins, Docker, and Kubernetes (EKS). The app is in the repo [Spring-BM](https://github.com/mostafaG95/Spring-BM.git).

## Prerequisites

- Docker installed on your local machine.
- Jenkins running with Docker CLI and kubectl installed.
- An AWS account with an EKS cluster set up.
- Docker Hub account for image storage.

## Use this File for Docker Image

Use the following `dockerfile` located in the repository to build the Docker image for jenkines with docker Cli , kubectl and aws:

```bash
docker build -f dockerfile -t jenk:1 .
docker run -d -p 8080:8080 -v /var/run/docker.sock:/var/run/docker.sock jenk:1


Here’s the updated code with the CI tasks included:

markdown
Copy code
## CI/CD for Spring Boot Application

This repository contains the CI/CD pipeline setup for a Spring Boot application using Jenkins, Docker, and Kubernetes (EKS). The app is in the repo **Spring-BM**.

### Prerequisites
- Docker installed on your local machine.
- Jenkins running with Docker CLI and kubectl installed.
- An AWS account with an EKS cluster set up.
- Docker Hub account for image storage.

### Use this File for Docker Image
Use the following Dockerfile located in the repository to build the Docker image for Jenkins with Docker CLI, kubectl, and AWS:

CI Tasks
I used Jenkins for CI tasks, including:

Unit testing
Building the Docker image
Pushing the image to Docker Hub

### use Jenkinsfile located in the repo 


  



