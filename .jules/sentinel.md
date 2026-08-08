# Sentinel Security Journal

This security journal is used by Sentinel to record critical learnings about
security vulnerabilities and hardening practices found in this repository.

## 2026-08-08 - Hardening GitHub Actions Workflow

**Vulnerability:** Excessively permissive default permissions for GITHUB_TOKEN
and insecure action references (using tags/branches instead of commit SHAs)
in the CI workflow can expose the repository to supply chain and write access
risks.

**Learning:** Unpinned actions can be silently updated by malicious actors, and
lack of top-level permissions on workflows default to permissive access
which could be exploited.

**Prevention:** Always pin GitHub Actions to full 40-character SHAs, explicitly
declare read-only top-level permissions, and set job execution timeouts.
