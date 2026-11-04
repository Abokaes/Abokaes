# Bolt Performance Journal

This journal records critical performance-related insights and learnings.

## 2026-11-03 - Optimizing CI Workflow Execution Efficiency

**Learning:** GitHub Actions workflows without concurrency controls and path
filters redundantly consume CI runners on documentation-only edits or rapid
successive commits.
**Action:** Configure `concurrency` cancellation for pull requests, apply
`paths-ignore` for non-build assets, and specify strict `timeout-minutes`.
