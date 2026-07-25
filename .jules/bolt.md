# Bolt Performance Journal

This journal is maintained by Bolt ⚡ to record critical performance-related
learnings and insights in this repository.

## 2026-07-24 - CI Optimization

**Learning:** Optimizing GitHub Actions workflows with concurrency limits and path
filtering prevents redundant and wasteful workflow runs on documentation and
non-functional file updates, saving valuable runner minutes.

**Action:** Implement `concurrency` blocks and `paths-ignore` logic in `.github`
workflow configurations.
