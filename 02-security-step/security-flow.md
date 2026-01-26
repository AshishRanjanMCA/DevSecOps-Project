# Security Workflow

## Logical Flow
1. Jenkins triggers security checks after build stage.
2. Trivy scans application files and Docker images.
3. Scan results are analyzed.
4. If critical vulnerabilities exist, pipeline stops.
5. kube-audit checks Kubernetes cluster security.
6. Only secure artifacts proceed to deployment stage.
