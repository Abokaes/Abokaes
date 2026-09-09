# Bolt Performance Journal

This journal records critical performance-related insights and learnings.

## 2026-08-22 - Optimizing GitHub Actions Workflow Efficiency

**Learning:** GitHub Actions workflows without concurrency limits, path filtering,
or job timeouts can cause redundant runner execution and resource waste.
**Action:** Always define concurrency groups with `cancel-in-progress: true`,
ignore non-functional documentation files (like README, LICENSE, `.jules/**`) in triggers,
and set job-level timeouts.
