# Continuous Integration and Deployment for Microservices

## Aim

To configure and implement an automated CI/CD pipeline that triggers on Git push events, builds Docker images, runs tests, and deploys microservices continuously and reliably.

---

## Problem Statement

Trigger a CI/CD pipeline using Git when code is pushed to the `develop` branch.

---

## Overview

This project demonstrates the implementation of a CI/CD pipeline for containerized microservices using GitHub Actions, Docker, and Git version control. The workflow automatically detects code changes pushed to the `develop` branch, triggers build automation, executes deployment workflows, and validates microservice delivery processes.

The project focuses on DevOps automation practices including continuous integration, automated build execution, containerized deployment workflows, and reliable software delivery.

---

## Technologies Used

* Git & GitHub
* GitHub Actions
* Docker
* Python
* Flask
* Linux

---

## Features

* Automated CI/CD workflow execution
* Git-based pipeline triggering
* Docker image build automation
* Continuous integration workflows
* Containerized deployment process
* Branch-based deployment management
* GitHub Actions automation
* Microservice deployment validation

---

## Workflow Architecture

```text
Developer Pushes Code
          ↓
GitHub Repository (develop branch)
          ↓
GitHub Actions Trigger
          ↓
Build Docker Image
          ↓
Run Validation Workflow
          ↓
Deploy Microservice
```

---

## Step 1: GitHub Repository Setup

Created a GitHub repository named `microservices-demo` and cloned it locally for development.

### Clone Repository

```bash id="vjlwm8"
git clone https://github.com/<your-username>/microservices-demo.git
cd microservices-demo
```

### Create Develop Branch

```bash id="g2fdqb"
git checkout -b develop
```

This setup enabled branch-based development workflows and automated pipeline triggering using Git events.

---

## Step 2: Create Microservice Application

Created a simple Flask-based microservice application and containerized it using Docker.

### Create Service Folder

```bash id="1ycx7u"
mkdir hello-service
cd hello-service
```

### Push Application Code

```bash id="9ojjlwm"
git add .
git commit -m "Added hello-service"
git push origin develop
```

The application code and Docker configuration were pushed to the `develop` branch to trigger the CI/CD pipeline automatically.

---

## Step 3: Configure GitHub Actions Workflow

Created a GitHub Actions workflow file to automate build and deployment workflows.

### Create Workflow Directory

```bash id="5v02m5"
mkdir -p .github/workflows
```

### Create Workflow File

```bash id="7x2g6k"
nano .github/workflows/deploy.yml
```

The workflow was configured to:

* detect push events on the `develop` branch
* install dependencies
* build Docker images
* validate deployment workflows
* automate CI/CD execution

---

## Step 4: Trigger Automated Pipeline

Committed and pushed the workflow configuration to GitHub.

```bash id="9e1r4p"
git add .github/workflows/deploy.yml
git commit -m "Add GitHub Actions workflow"
git push origin develop
```

GitHub Actions automatically detected the push event and executed the CI/CD workflow through the Actions tab.

---

## Learning Outcomes

* Understanding CI/CD pipeline implementation
* Working with GitHub Actions automation
* Docker-based deployment workflows
* Git-triggered automation pipelines
* Branch-based development workflows
* Continuous integration concepts
* Automated microservice deployment
* DevOps automation practices

---

## Conclusion

Successfully implemented a CI/CD pipeline for a containerized microservice using GitHub Actions and Docker. The workflow automatically triggered on Git push events, executed build automation, and validated deployment workflows, demonstrating core DevOps and continuous delivery concepts.

---

## Author

Sruja Pisal
