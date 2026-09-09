# Bolt Performance Journal

This journal records critical performance learnings and optimizations to make
sure we avoid regressions and design with efficiency in mind.

## 2026-07-30 - Optimize CI Workflow Efficiency

**Learning:** GitHub Actions workflows default to executing on every push and
pull request, regardless of whether the changes affect functional code or
documentation (e.g., README.md, LICENSE). Additionally, lacking concurrency control
means multiple commits sequentially push redundant pipeline runs that consume
valuable execution minutes.

**Action:** Implement top-level concurrency groups with `cancel-in-progress:
true` to drop redundant builds, filter out non-functional directories from
triggering the workflow, and add a reasonable step timeout of 5 minutes to
safeguard resources.
