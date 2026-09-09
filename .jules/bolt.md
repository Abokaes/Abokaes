# Bolt Performance Journal

This journal records critical learnings about performance optimizations made in
this repository.

## 2026-08-06 - Optimized CI/CD Workflow Execution Time

**Learning:** Unnecessary and redundant GitHub Actions workflow executions can
be eliminated using path filtering and concurrency control, reducing wasted
runner minutes.

**Action:** Add `paths-ignore` and a concurrency group with
`cancel-in-progress: true` in workflow configurations.
