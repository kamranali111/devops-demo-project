# DevOps Demo Project

This project demonstrates how to set up a complete DevOps CI/CD pipeline locally using a variety of tools and technologies, including GitHub, Jenkins, Maven, SonarQube, Docker, DockerHub, ArgoCD, Helm, Kubernetes, Prometheus, Grafana, Filebeat, OpenSearch, and Kibana.

![Flow Diagram](https://github.com/deepakkr35/devops-demo-project/blob/main/devops-demo-project.gif)



## Project Overview

The goal of this project is to provide a comprehensive guide for setting up a local DevOps pipeline that covers code management, build automation, containerization, static code analysis, deployment, monitoring, and logging. It is designed for developers and DevOps engineers who want to practice setting up a CI/CD pipeline using modern DevOps tools.

### Tools and Technologies

- **Version Control:** GitHub
- **CI/CD Tool:** Jenkins
- **Build Tool:** Maven
- **Static Code Analysis:** SonarQube
- **Containerization:** Docker
- **Container Registry:** DockerHub
- **Deployment Automation:** ArgoCD
- **Package Management:** Helm
- **Container Orchestration:** Kubernetes
- **Monitoring:** Prometheus, Grafana
- **Logging:** Filebeat, OpenSearch, Kibana

## Prerequisites

Before setting up the pipeline, make sure you have the following installed locally:

- **Git**
- **Docker & Docker Compose**
- **Java 11+** (for building Java applications)
- **Maven**
- **Jenkins**
- **SonarQube**
- **Kubernetes Cluster** (e.g., Minikube, Kind, or Docker Desktop with Kubernetes)
- **ArgoCD**
- **Helm**
- **Prometheus & Grafana**
- **Filebeat, OpenSearch & Kibana**

## Pipeline Stages

1. **Source Code Management**: 
   - Host your application code on GitHub.
   - This project uses a simple Java application stored in a GitHub repository.

2. **Build and Test**:
   - Jenkins clones the repository and uses Maven to build the project.
   - The Maven `clean package` command is used to build the JAR file.
   
3. **Static Code Analysis**:
   - SonarQube is used to analyze the code quality.
   - Jenkins integrates with SonarQube to run the analysis and view results.
   
4. **Build Docker Image**:
   - Jenkins builds a Docker image for the Java application.
   - The image is tagged using the build version parameter and pushed to DockerHub.

5. **Deployment**:
   - ArgoCD is used to automate the deployment of the Docker image to a Kubernetes cluster.
   - Helm is used for managing Kubernetes resources (e.g., deployments, services).
   
6. **Monitoring**:
   - Prometheus is used to collect metrics from the Kubernetes cluster.
   - Grafana provides a dashboard for visualizing these metrics.
   
7. **Logging**:
   - Filebeat collects logs from the application and sends them to OpenSearch.
   - Kibana is used for visualizing and querying logs in OpenSearch.

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/devops-demo-project.git
cd devops-demo-project
