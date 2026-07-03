# Sentinel Security Journal

## 2026-07-03 - GitHub Actions Hardening Pattern
**Vulnerability:** Default GITHUB_TOKEN permissions are overly permissive, and mutable action tags are susceptible to supply chain attacks.
**Learning:** Hardening CI/CD workflows is a critical layer of defense-in-depth, even for simple repositories.
**Prevention:** Always set explicit `permissions`, include `timeout-minutes` for jobs, and pin actions to specific commit SHAs.
