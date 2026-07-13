# Sentinel Security Journal

This journal is used by Sentinel 🛡️ to record critical security learnings, vulnerability patterns, and reusable security practices discovered within this repository.

## 2026-07-12 - GitHub Actions Workflow Hardening
**Vulnerability:** Default GitHub Actions permissions are often overly permissive, and mutable tags for actions can lead to supply chain attacks.
**Learning:** Hardening CI/CD pipelines is a foundational security step even in minimalist repositories. Pinning actions to SHAs and restricting token permissions follows the principle of least privilege.
**Prevention:** Always set explicit permissions (e.g., `contents: read`), define job timeouts, and pin actions to specific SHAs in workflow files.
