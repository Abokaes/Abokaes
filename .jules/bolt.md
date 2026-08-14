# Bolt Performance Journal

This journal records critical performance-related learnings to help make better
decisions and avoid performance mistakes in this repository.

## 2026-08-14 - Optimize CI Workflow Execution

**Learning:** Running CI workflows on non-functional files like README.md and
LICENSE or allowing multiple concurrent builds on the same branch wastes
substantial CI runner time and resources.

**Action:** Implement concurrency cancellation, paths-ignore for non-functional
assets, and standard job-level timeouts to optimize runner utilization and
minimize pipeline latency.
