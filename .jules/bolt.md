# Bolt Performance Journal

This journal records critical learnings related to performance optimizations,
including bottlenecks, failed attempts, and codebase-specific patterns.

## 2026-08-09 - GitHub Actions CI Optimization

**Learning:** GitHub Actions workflows can be optimized for both execution speed
and security. Implementing top-level concurrency limits redundant parallel execution,
while path filtering prevents CI runs on non-functional documentation updates,
saving runner minutes. Using precise job-level timeouts prevents hung runners
from consuming excessive resources, and pinning Actions to specific SHAs secures the environment.

**Action:** Add `concurrency` blocks, `paths-ignore` filters, and job `timeout-minutes`
to the repository's workflows.
