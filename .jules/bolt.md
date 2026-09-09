# Bolt Performance Journal

This journal records critical performance-related learnings and insights across
the repository.

## 2026-08-14 - GitHub Actions Workflow Optimization

**Learning:** GitHub Actions workflows without concurrency control, path
filtering, or job timeouts waste runner resources and slow down feedback loops
on redundant commits.
**Action:** Always configure `concurrency` with `cancel-in-progress: true`,
`paths-ignore` for non-functional files (documentation, licenses, metadata), and
`timeout-minutes` on jobs.
