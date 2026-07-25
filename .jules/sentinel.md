# Sentinel Security Journal

This journal is maintained by Sentinel <span role="img" aria-label="shield">🛡️</span> to record critical security-related learnings.

## 2026-07-24 - Workflow Hardening and Least Privilege

**Vulnerability:** Excess permissions and unpinned software versions in the
GitHub Actions CI/CD workflows, leaving the repository open to supply chain or execution attacks.

**Learning:** When using default or overly broad settings in CI workflows, external dependencies can be modified or compromised. Restricting repository permissions at the top-level forces job isolation, and pinning checkout actions to an immutable commit SHA prevents unauthorized action updates.

**Prevention:** Always declare top-level read-only permissions and pin external actions using secure commit SHAs.
