# Banque-misr

## CI/CD for Spring Boot Application

This repository contains the CI/CD pipeline setup for a Spring Boot application using Jenkins, Docker, and Kubernetes (EKS). The app is in the repo [Spring-BM](https://github.com/mostafaG95/Spring-BM.git).

## Prerequisites

- Docker installed on your local machine.
- Jenkins running with Docker CLI and kubectl installed.
- An AWS account with an EKS cluster set up.
- Docker Hub account for image storage.

## Use this File for Docker Image

Use the following `dockerfile` located in the repository to build the Docker image for Jenkins with Docker CLI, kubectl, and AWS:

```bash
docker build -f dockerfile -t jenk:1 .
docker run -d -p 8080:8080 -v /var/run/docker.sock:/var/run/docker.sock jenk:1
```
## CI Tasks

I used Jenkins for CI tasks, including:

- **Unit Testing**: Running tests to ensure code quality.
- **Building the Docker Image**: Creating an image for the application.
- **Pushing the Image to Docker Hub**: Storing the image for deployment.
- Use the following `Jenkinsfile` located in the repository for CI pipeline



  



