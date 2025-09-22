# Rablo-Devops-Project
# Rablo DevOps Project

## Overview

This project demonstrates deployment of a simple Node.js application using Docker containers, automated with CI/CD pipelines using Jenkins and GitHub Actions. Application is deployed on AWS EC2 instances behind an Application Load Balancer (ALB).

## Project Structure

- `rablo-devops-assignment/docker-app` - Node.js app source and Dockerfile
- `Jenkinsfile` - Jenkins CI/CD pipeline script for build and deploy
- `.github/workflows/ci-cd.yml` - GitHub Actions workflow for automated build, push, and deploy
- `README.md` - Project documentation

## Prerequisites

- Docker, Docker Hub account
- AWS account and EC2 instances
- Jenkins server (optional)
- GitHub repo with configured secrets (DockerHub credentials, EC2 SSH key)

## CI/CD Pipelines

- **Jenkins:** Builds Docker image, pushes to Docker Hub, deploys containers on EC2 using SSH commands.
- **GitHub Actions:** Runs on commits to `main` branch, performs the same tasks automatically with secrets.

## Deployment

- Application runs as Docker containers on AWS EC2 instances.
- A load balancer (ALB) distributes traffic to instances running containers on port 80.
- Application returns "Hello World" at the root URL.

## How to Run

1. Clone this repo
2. Setup secrets and credentials as per pipeline files
3. Push changes to trigger GitHub Actions or run Jenkins pipeline
4. Access application using EC2 public IP or ALB DNS name

## Troubleshooting

- Ensure `docker-app` folder is correctly referenced in workflow context
- Set proper AWS security groups and key permissions
- Verify credential secrets for DockerHub and EC2

---

For detailed setup and screenshots, refer to `/docs` folder or project documentation files.

