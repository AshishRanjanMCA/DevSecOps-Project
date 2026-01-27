# Trivy Vulnerability Scanning

## Purpose
Trivy is used to perform **vulnerability scanning** on application file systems and Docker images as part of the security stage in the CI/CD pipeline.  
This ensures that known security vulnerabilities are detected before deployment.

---

## Execution Context
Trivy is executed on the **Jenkins server** and is fully integrated into the CI/CD pipeline.

---

## Scan Types

### File System Scan
- Scans application source code and dependencies
- Detects known vulnerabilities in libraries and packages
- Helps identify issues early in the build process

### Docker Image Scan
- Scans container images built during the pipeline
- Identifies vulnerabilities in base images and installed packages
- Prevents deployment of insecure container images

---

## Pipeline Integration
1. Jenkins triggers the Trivy scan after the build stage completes.
2. Trivy performs file system and Docker image scans.
3. Scan results are evaluated based on severity levels.
4. If **critical or high-severity vulnerabilities** are detected, the pipeline fails.
5. Only vulnerability-free artifacts proceed to the next pipeline stage.

---

## Security Outcome
- Early detection of security vulnerabilities
- Automated enforcement of security policies
- Reduced risk of deploying insecure applications

---

## Reference
For Trivy installation and configuration details, refer to:  
[Security Tools Setup](../docs/security-tools.md)
