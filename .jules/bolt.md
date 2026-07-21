# Bolt Performance Journal

This journal records critical performance learnings, bottlenecks, and
optimizations in this codebase.

## 2026-07-17 - Optimize CI Workflow Execution

**Learning:** Unoptimized CI configurations run redundant workflows on non-code
changes (like Markdown edits and licensing files) and lack concurrency controls,
leading to wasted compute and slow overall delivery times.

**Action:** Configure concurrency groups with `cancel-in-progress: true` and
implement path filtering (`paths-ignore`) to ignore non-functional changes in
GitHub Actions, coupled with securing the environment using top-level read-only
permissions and job timeouts.
