# Bolt Performance Journal

This journal records critical performance learnings and optimizations to make things
lightning fast.

## 2026-07-29 - Optimize CI Workflows with Concurrency and Path Filtering

**Learning:** CI workflows run on every push and pull request, consuming valuable
runner compute resources and time. By introducing concurrency cancellation, we
can immediately abort redundant, out-of-date jobs. By adding path filtering,
we can completely skip expensive runner instantiation and step execution for
non-functional changes (like documentation or journal updates).

**Action:** Add top-level concurrency configuration and paths-ignore filters
to the CI workflow.
