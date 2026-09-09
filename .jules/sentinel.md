# Sentinel Security Journal

This journal records critical security learnings, findings, and prevention strategies for the repository.

## 2026-08-14 - Repository Security Hardening & Baseline

**Vulnerability:** Unconstrained workflow permissions, unpinned third-party actions, lack of job timeouts in CI/CD pipelines, missing `.gitignore`, and absent security vulnerability reporting policy.
**Learning:** Default GITHUB_TOKEN permissions in GitHub Actions can expose repository contents or secrets if a step is compromised. Unpinned actions rely on mutable tags which pose supply chain risks.
**Prevention:** Always declare explicit top-level permissions (`contents: read`), pin actions to full commit SHAs, set explicit job timeouts, and maintain `.gitignore` and `SECURITY.md`.
