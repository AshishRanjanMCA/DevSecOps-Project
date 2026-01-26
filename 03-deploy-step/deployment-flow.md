# Kubernetes Deployment Flow

1. Jenkins triggers deployment stage.
2. kubectl applies Kubernetes manifests.
3. Kubernetes scheduler assigns Pods to worker nodes.
4. Application Pods start running.
5. Service exposes the application.
