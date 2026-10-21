# Sprint 3 Static Code Analysis — BJJ Fitness App

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
| Bugs (reliability issues) | 9 |
| Vulnerabilities (security issues) | 6 |
| Code Smells (maintainability issues) | 0 |
| Security Hotspots | 0 |
| Quality Gate | Passed |

### Trivy

| Severity | Count |
|---|---:|
| CRITICAL | 0 |
| HIGH | 0 |
| MEDIUM | 0 |
| LOW | 0 |

## 3. Scope

- **SonarQube:** Scanned the repository from its root (`sonar.sources=.`), excluding generated files, build artifacts, `.git`, Pods, and generated Dart files.
- **Trivy:** Scanned the repository filesystem. Vulnerability results covered `pubspec.lock` and `lib/pubspec.lock`; no supported configuration files were detected.

## 4. Trend (If Applicable)

Baseline sprint - no prior static analysis results available for comparison.

## 5. Reflection (Short)

The most problematic area was security, with six issues reported by SonarQube, including three high-severity findings involving GitHub Actions dependencies and Android release configuration. Next sprint, we plan to review these findings, pin workflow dependencies to full commit hashes, and improve the Android release configuration.

## Required Statement

“This static analysis was generated using automated tools during this sprint.”
