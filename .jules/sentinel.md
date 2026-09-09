# Sentinel Security Journal

This journal tracks critical security learnings, vulnerability patterns, and
security-focused architectural gaps identified by Sentinel 🛡️ in this
repository.

## 2026-07-14 - Hardening CI/CD Workflows

**Vulnerability:** Use of mutable tags for GitHub Actions and overly permissive
default GITHUB_TOKEN permissions.
**Learning:** Relying on version tags (like `@v4`) in GitHub Actions makes the
workflow susceptible to supply chain attacks if the tag is moved to a malicious
commit. Additionally, default permissions for the GITHUB_TOKEN can be
excessively broad, increasing the impact of a compromised workflow.
**Prevention:** Pin all GitHub Actions to a specific commit SHA and implement
the principle of least privilege by explicitly defining required permissions
(e.g., `contents: read`) at the workflow or job level.
