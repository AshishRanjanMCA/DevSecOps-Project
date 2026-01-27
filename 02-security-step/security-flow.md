# Security Flow (DevSecOps Stage)

## Purpose
The **Security Flow** ensures that applications and infrastructure are scanned for vulnerabilities before deployment.  
This stage enforces DevSecOps principles by integrating security checks directly into the CI/CD pipeline.

---

## Security Tools Used
- **Trivy** – File system and container image vulnerability scanning
- **kube-audit** – Kubernetes cluster security auditing
- **Jenkins** – Orchestrates security checks as part of the pipeline

---

## Logical Security Flow
1. Jenkins triggers the security stage after the successful build phase.
2. Trivy scans application files and Docker images for known vulnerabilities.
3. Scan results are analyzed based on severity levels.
4. If critical or high-severity vulnerabilities are detected, the pipeline is stopped.
5. kube-audit evaluates Kubernetes cluster configurations against security best practices.
6. Only verified and secure artifacts are allowed to proceed to the deployment stage.

---

## Security Outcome
- Vulnerabilities detected early in the pipeline
- Prevention of insecure deployments
- Improved cluster and application security posture

---

## Reference
For security tool installation and configuration, refer to:
[Security Tools Setup](../docs/security-tools.md)
