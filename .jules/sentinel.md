# Sentinel Security Journal

This security journal is used to record critical security-related learnings
and vulnerability details identified during security reviews and hardening
operations.

## 2026-07-30 - GitHub Actions Workflow Hardening

**Vulnerability:** Excessively permissive GitHub Actions workflow permissions,
lack of step timeouts, and unpinned action SHA dependencies.
**Learning:** Default workflow tokens have read/write access to the repository,
which poses a significant security risk if a step or upstream dependency is
compromised. Unpinned third-party actions can be updated or hijacked in supply
chain attacks.
**Prevention:** Always restrict top-level workflow permissions to `contents:
read` (unless write is explicitly required), pin third-party actions to known,
validated full commit SHAs, and set explicit timeouts for all execution steps
or jobs to prevent denial of service or excessive resource usage.
