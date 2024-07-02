# Ekart CI/CD Pipeline

This repository contains the Jenkins CI/CD pipeline configuration for the Ekart project. The pipeline automates the process of building, testing, and deploying the application.

## Project Overview

The CI pipeline includes the following stages:
1. **Checkout Code**: Fetch code from GitHub.
2. **Code Quality Analysis**: Perform static code analysis using SonarQube.
3. **Dependency Checks**: Analyze project dependencies for vulnerabilities using OWASP Dependency-Check.
4. **Build Docker Image**: Build a Docker image of the application.
5. **Push Docker Image**: Push the Docker image to Docker Hub.
6. **Trigger CD Pipeline**: Trigger the CD pipeline to deploy the Docker image.

The CD pipeline includes:
1. **Pull Docker Image**: Pull the Docker image from Docker Hub.
2. **Deploy Application**: Deploy the application container.

## Setup Instructions

### Prerequisites
- Jenkins
- SonarQube
- Docker
- Docker Hub Account

### Jenkins Setup
1. Install Jenkins and the necessary plugins (e.g., Git, Docker, SonarQube Scanner).
2. Create and configure the necessary credentials (GitHub, Docker Hub, SonarQube).

### SonarQube Setup
1. Install and configure SonarQube.
2. Create a new project in SonarQube for analysis.

### Running the Pipeline
1. Clone this repository.
2. Import the Jenkinsfile into a Jenkins pipeline job.
3. Run the pipeline.

## Reports

### OWASP Dependency-Check Report

The OWASP Dependency-Check report is included in this repository to demonstrate the analysis of project dependencies for vulnerabilities.

## Demonstration

### GitHub Repository
[GitHub Project Link](https://github.com/jaiswaladi246/Ekart)
For Details follow link(https://www.youtube.com/watch?v=jbEF3mB7UcU&t=1s)

### Docker Hub
[Docker Hub Repository](https://hub.docker.com/r/firestorm001/ekart)

## Running App ##
To pull the Docker image from Docker Hub and run the application as a container on localhost:8070, use the following commands:
 - docker pull firestorm001/ekart:latest
 - docker run -d -p 8070:8070 --name=ekart <ekart_image_id>

 ## Ekart Login ##
 username : admin
 password : admin
