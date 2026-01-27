
---

# docs/jenkins-setup.md

```md
# Jenkins Setup

This document explains the installation and configuration of **Jenkins** as the CI/CD orchestrator.

## Jenkins Server Setup
- Install Java (JDK 17)
- Install Jenkins and start the service on port 8080
- Install Docker and configure user permissions
- Install kubectl to enable Kubernetes deployments
- Install Trivy for security scanning
- Install Node Exporter to expose system metrics

## Jenkins Pipeline Responsibilities
- Trigger builds via Git webhook
- Perform static code analysis
- Run security scans
- Build Docker images
- Push artifacts to Nexus
- Deploy applications to Kubernetes

## Outcome
Automated CI/CD pipeline with integrated security and deployment.

