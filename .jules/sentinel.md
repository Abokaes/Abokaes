## 2026-03-05 - GitHub Actions Hardening
**Vulnerability:** Default GITHUB_TOKEN permissions are overly permissive, workflows without timeouts can cause resource exhaustion, and action tags can be moved (supply chain risk).
**Learning:** Hardening workflows at the source is the first line of defense for CI/CD pipelines.
**Prevention:** Always define explicit `permissions`, set `timeout-minutes` on jobs, and pin actions to specific commit hashes (SHAs).
