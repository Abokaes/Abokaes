# Bolt Performance Journal

## 2026-08-14 - GitHub Actions Concurrency & Path Filtering Optimization

**Learning:** In profile and documentation-centric repositories, CI workflows
often waste runner execution minutes on non-code changes (such as README or
journal updates) and on redundant intermediate pushes.
**Action:** Always configure `paths-ignore` for non-code assets (`README.md`,
`LICENSE`, `.jules/**`) and top-level `concurrency` with
`cancel-in-progress: true` in workflow definitions.
