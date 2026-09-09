# Bolt Performance Journal

This journal records critical performance learnings, bottlenecks, and results
of optimization efforts to make things lightning fast.

## 2026-07-17 - GitHub Actions Path Filtering and Concurrency

**Learning:** Unnecessary CI workflow runs trigger on modifications to non-
functional files like README, LICENSE, or journal entries, wasting runner hours
and delay feedback. In addition, consecutive push events build in parallel
instead of auto-cancelling.

**Action:** Configure concurrency groups to cancel in-progress runs on the same
ref and specify path filtering using `paths-ignore` on the push and
pull_request triggers.
