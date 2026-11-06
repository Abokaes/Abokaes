# Sentinel Security Journal

This journal tracks critical security discoveries, vulnerabilities, and
hardening patterns identified across the repository.

## 2026-11-03 - Supply Chain Hardening and Permissions in GitHub Actions

**Vulnerability:** Default broad GITHUB_TOKEN permissions, mutable action tags
(`actions/checkout@v4`), and unbounded execution timeouts in CI workflows.
**Learning:** Default GitHub Actions workflows can be vulnerable to tag-spoofing
supply chain attacks and unnecessary write/admin permissions granted by default
repository token configurations. Lack of timeouts also introduces DoS risk.
**Prevention:** Always enforce explicit least-privilege token permissions
(`permissions: contents: read`), pin action references to immutable commit
SHAs, and specify execution timeouts (`timeout-minutes`).
