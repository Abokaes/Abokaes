# Bolt Performance Journal

This journal records critical performance-related insights and optimization
learnings to avoid regressions and guide future work.

## 2026-07-29 - CI Workflow Optimization

**Learning:** GitHub Actions workflows can be slow and waste runner time on
non-functional changes (such as README updates) or when multiple pushes occur
simultaneously. Implementing concurrency checks and path-ignore filters is
critical to make CI fast and cost-effective.

**Action:** Configure concurrency groups to cancel in-progress runs, set job
timeouts, and ignore non-code files like README.md and .jules/ in the CI
trigger configuration.
