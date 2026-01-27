
# Nexus Setup

This document describes the setup of **Nexus Repository Manager** for artifact storage.

## Installation Method
- Install Docker engine
- Run Nexus as a Docker container:
  ```bash
  docker run -d \
    -p 8081:8081 \
    --name nexus \
    sonatype/nexus3

## Configuration

Create repositories for:
- Maven artifacts
- Docker images
Configure Jenkins credentials for Nexus access

## Outcome

Centralized artifact and container image repository.
