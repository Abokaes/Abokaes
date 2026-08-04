# Bolt Performance Journal

This journal is maintained by Bolt ⚡ to record critical performance-related
learnings and insights discovered during optimizations of this codebase.

## 2026-08-03 - CI/CD Workflow Performance Optimization

**Learning:** Unoptimized CI pipelines can run redundant builds and tests for
unrelated changes, consuming resources and slowing down feedback loops.

**Action:** Implement concurrency control to cancel in-progress runs when a new
push occurs, add path filtering to ignore non-code files (e.g. documentation,
license), and enforce job timeouts to prevent hung tasks.
