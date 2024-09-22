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
docker build -t jenk .


  



