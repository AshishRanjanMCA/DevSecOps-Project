# Code Quality Stage (SonarQube)

## Purpose
The **Code Quality Stage** ensures that source code meets defined quality standards before it proceeds further in the CI/CD pipeline.  
This stage helps detect bugs, code smells, and maintainability issues early in the development lifecycle.

---

## Role of SonarQube in the Build Stage
SonarQube is integrated with Jenkins to perform **static code quality analysis** during the build phase.

---

## Code Quality Responsibilities
- Analyze source code using static analysis rules
- Detect bugs, vulnerabilities, and code smells
- Enforce quality gates (pass/fail conditions)
- Provide detailed code quality reports
- Block the pipeline if quality thresholds are not met

---

## Build Flow Integration
1. Jenkins pulls the latest source code from the repository.
2. Jenkins triggers SonarQube analysis as part of the build pipeline.
3. SonarQube evaluates the code against configured quality gates.
4. Jenkins receives the analysis result.
5. If quality checks pass, the pipeline continues to the next stage.

---

## Output of This Stage
- Code quality reports
- Quality gate status (pass/fail)
- Improved and maintainable codebase

---

## Reference
For SonarQube installation and configuration details, refer to:  
[SonarQube Setup](../docs/sonarqube-setup.md)
