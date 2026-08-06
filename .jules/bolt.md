# Bolt Performance Journal

This journal records critical performance-related learnings to help make
the codebase faster, one optimization at a time.

## 2026-08-05 - GitHub Actions Workflow Optimization

**Learning:** Workflows in simple repositories often run on every push and PR
regardless of whether the changed files actually impact build or deployment,
wasting valuable runner time. Adding path filtering and concurrency controls
significantly reduces redundant workflow executions.

**Action:** Implement `paths-ignore` for non-functional files like README,
LICENSE, and the `.jules/` directory, and apply a top-level concurrency group to
automatically cancel outdated pipeline runs.
