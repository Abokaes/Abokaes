# Bolt Performance Journal

This journal records critical performance learnings and insights discovered while optimizing the repository.

## 2026-08-14 - CI Workflow Optimization with Concurrency and Path Filtering
**Learning:** CI runner minutes and build queue times are wasted when non-code files (like documentation or journal entries) trigger full workflow runs, or when outdated commits on the same branch continue running in parallel.
**Action:** Always configure top-level concurrency with `cancel-in-progress: true` and `paths-ignore` for non-code files in GitHub Actions workflows.
