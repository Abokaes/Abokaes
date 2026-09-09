# Bolt Performance Journal

This journal is maintained by Bolt ⚡ to record critical performance-related
learnings and insights discovered during optimizations of this codebase.

## 2026-08-09 - Optimize CI Workflow Execution and Efficiency

**Learning:** Unoptimized CI pipelines run redundant builds for minor or
documentation changes and allow duplicate builds to run concurrently,
consuming scarce runner credits.
**Action:** Apply strict concurrency cancel-in-progress controls, job-level
timeouts, and ignore non-code paths on workflow triggers.
