# Sentinel Security Journal

This security journal is used to record critical security-related learnings
and vulnerability patterns discovered in this codebase.

## 2026-08-06 - Hardened CI Workflows and Actions Permissions

**Vulnerability:** Overly permissive GitHub Actions workflows and unpinned
third-party actions expose the CI/CD pipeline to unauthorized repository
modifications and potential supply chain attacks.

**Learning:** Default workflow permissions (`GITHUB_TOKEN`) are often set to
read/write, which can be exploited if a step is compromised. Unpinned actions
referencing branches/tags (e.g., `v4`) can change without warning, whereas a
specific commit SHA guarantees exactly what code runs.

**Prevention:** Explicitly define the minimum required top-level permissions in
all GitHub workflows (`permissions: contents: read`), pin actions to a specific
commit SHA, enforce short job timeouts (e.g., `timeout-minutes: 5`), and add
concurrency controls to prevent parallel race conditions or wasting resources.
