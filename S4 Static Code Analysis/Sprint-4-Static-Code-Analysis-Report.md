# Sprint 4 Static Code Analysis — BJJ Fitness App

## 1. Tools Used

- **Programming languages:** Dart (Flutter), Kotlin (Android configuration), YAML (GitHub Actions).
- **SonarQube:** SonarQube Cloud — Advanced Security.
- **SonarQube execution:** GitHub Actions CI on Ubuntu, `main` branch.
- **Trivy:** Version 0.76.0; filesystem scan for vulnerabilities and misconfigurations.
- **Trivy execution:** Locally in VS Code using Windows PowerShell.

## 2. Required Metrics

### SonarQube

| Metric | Count / Status |
|---|---:|
| Bugs (reliability issues) | 4 |
| Vulnerabilities (security issues) | 0 |
| Code Smells (maintainability issues) | 0 |
| Security Hotspots | 0 |
| Quality Gate | Failed |

### Trivy

| Severity | Count |
|---|---:|
| CRITICAL | 0 |
| HIGH | 0 |
| MEDIUM | 0 |
| LOW | 0 |

## 3. Scope

- **SonarQube:** Scanned the Flutter application source code (`sonar.sources=lib`) and included tests from the `test` directory. Excluded generated files, build artifacts, `.git`, Pods, and generated Dart files. Coverage reporting was configured using `coverage/lcov.info`.
- **Trivy:** Scanned the repository filesystem for vulnerabilities and misconfigurations. Vulnerability results covered `pubspec.lock` and `lib/pubspec.lock`, with no vulnerabilities detected.

## 4. Trend

Compared with Sprint 3, reliability issues decreased from 9 to 4, and security issues decreased from 6 to 0. Maintainability issues and security hotspots remained at 0. Trivy continued to report no vulnerabilities across all four severity levels. However, the SonarQube Quality Gate changed from Passed to Failed because new code coverage was 45.32%, below the required 80%.

## 5. Reflection (Short)

The main challenge this sprint was automated test coverage, although security and reliability findings decreased, the Quality Gate failed due to insufficient coverage. Next sprint, we plan to expand automated tests for the new features and address the four remaining reliability issues in the Recovery screen.

## Required Statement

“This static analysis was generated using automated tools during this sprint.”
