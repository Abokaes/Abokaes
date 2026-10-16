# Bolt Performance Journal

This journal records critical performance learnings and insights discovered while optimizing the codebase.

## 2026-08-14 - CI Workflow Optimization via Concurrency and Path Filtering
**Learning:** In repositories without application source code, GitHub Actions CI runs on non-code changes (documentation, markdown, license) and redundant concurrent pushes, wasting runner execution minutes.
**Action:** Always add top-level `concurrency` with `cancel-in-progress: true` and `paths-ignore` for non-code files (`README.md`, `LICENSE`, `.jules/**`) to prevent unnecessary workflow triggers and cancel outdated builds immediately.
