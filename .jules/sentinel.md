# Sentinel Security Journal

This security journal is used to record critical security-related learnings
and prevention measures implemented in this repository.

## 2026-07-24 - Secure GitHub Actions Workflow Hardening

**Vulnerability:** Weak default GitHub Actions permissions and missing runtime
constraints on blank.yml workflow, allowing potential token permissions
escalation or Denial of Service/unlimited runs.

**Learning:** GitHub Actions workflows by default can have broad permissions if
not explicitly locked down with top-level `permissions: contents: read`. Adding
explicit job-level timeouts preventing hanging jobs from wasting actions runner
minutes is also crucial for robust CI health.

**Prevention:** Always declare top-level permissions, use job-level timeouts,
pin 3rd party actions to full commit hashes instead of tags, and define
sensible workflow concurrency groups.
