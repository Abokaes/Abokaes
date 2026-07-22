# Bolt Performance Journal

This journal records critical performance learnings and optimizations.

## 2026-07-17 - GitHub Actions CI Optimization

**Learning:** Unnecessary CI workflow runs on documentation and non-code file
updates waste runner execution time and resources. Adding path-filtering to
ignore README.md, LICENSE, and .jules/** files, coupled with concurrency
controls and timeout limits, significantly improves CI resource utilization and
response.

**Action:** Ensure all CI workflows implement proper path filtering and
concurrency controls.
