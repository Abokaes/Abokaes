# Bolt Performance Journal

This journal is used to record critical performance-related learnings
and insights for Bolt ⚡.

## 2026-08-01 - CI Workflow Concurrency and Path Filtering

**Learning:** GitHub Actions workflow minutes can be wasted running tests on
non-functional files (like markdown documentation and licenses) and on obsolete
git refs when multiple commits are pushed in rapid succession.

**Action:** Always implement `paths-ignore` for documentation and metadata
paths, and define a top-level `concurrency` block with
`cancel-in-progress: true` to optimize workflow execution resources and reduce
latency. Keep job timeouts minimal (e.g., `timeout-minutes: 5`) to prevent
hanging jobs from consuming entire runner pools.
