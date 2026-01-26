### Project Architecture Diagram

![Project Architecture Diagram](project-architecture.png)

### Project Architecture Diagram (Logical View)
+--------------------------------------------------+
|              Kubernetes Cluster                  |
|                                                  |
|   +-------------+                                |
|   | Master Node |                                |
|   +-------------+                                |
|        |                                         |
|  -------------------------                       |
|  |                       |                      |
|+-----------+       +-----------+                |
|| Worker 1  |       | Worker 2  |                |
|+-----------+       +-----------+                |
|                                                  |
+--------------------------------------------------+
                ↑
                |
        Deployment via kubectl
                |
+--------------------------------------------------+
|                DevOps Tools Layer                |
|                                                  |
|   +-----------+                                  |
|   | Jenkins   |  (CI/CD Orchestrator)            |
|   +-----------+                                  |
|     |       |                                    |
|     |       +------------------+                 |
|     |                          |                 |
|+------------+          +------------+            |
|| SonarQube  |          |   Nexus    |            |
|| Code Scan  |          | Artifacts  |            |
|+------------+          +------------+            |
|                                                  |
+--------------------------------------------------+
                |
                | Metrics & Health Data
                ↓
+--------------------------------------------------+
|               Monitoring Layer                   |
|                                                  |
|      Prometheus  <---- metrics collection        |
|            |                                     |
|         Grafana  ----> dashboards                |
|                                                  |
+--------------------------------------------------+

### Architecture Overview

This project follows a layered DevSecOps Architecture.

- The Kubernetes Cluster consists of one Master node and two Worker nodes.
- Jenkins acts as the CI/CD orchestrator and manages the pipeline.
- SonarQube performs static code analysis during the build stage.
- Nexus stores build artifacts and Docker images.
- Jenkins deploys applications to the Kubernetes cluster using kubectl.
- Prometheus collects metrics from Jenkins and application endpoints.
- Grafana visualizes system and application metrics using dashboards.

