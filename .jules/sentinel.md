# Sentinel Security Journal

This journal records critical security-related learnings, vulnerability findings, and architectural constraints discovered in this repository.

## 2026-08-14 - Initial Security Journal Baseline
**Vulnerability:** Default CI workflow lacked strict permissions, timeout bounds, and commit SHA action pinning.
**Learning:** Default GitHub Actions workflow templates grant implicit write permissions and lack defense-in-depth security controls.
**Prevention:** Always enforce explicit `permissions: contents: read`, set job-level timeouts, and pin third-party actions to immutable commit SHAs.
