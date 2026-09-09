# Bolt Performance Journal

This journal records critical performance-related insights and learnings.

## 2026-07-24 - Optimizing GitHub Actions Workflow

**Learning:** GitHub Actions workflows without concurrency limits, path filtering,
or job timeouts can cause redundant runner execution and resource waste.
**Action:** Always define concurrency groups with `cancel-in-progress: true`,
ignore non-functional files (like docs) in triggers, and set job-level
timeouts.
