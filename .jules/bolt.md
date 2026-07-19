# Bolt Performance Journal

This journal records critical learnings, insights, and actions taken to
optimize codebase performance, eliminate bottlenecks, and ensure extremely
efficient execution.

## 2026-07-17 - GitHub Actions CI Performance Optimization

**Learning:** GitHub Action workflow runs trigger on every push and pull
request by default. For repository documentation or meta files (like
`README.md`, `LICENSE`, or `.jules/**`), running full CI workflows is
redundant and wastes runner resources/time. Additionally, concurrent workflow
runs on the same branch can queue or execute unnecessarily when newer runs
supersede them.

**Action:** Implement top-level `concurrency` control to cancel running builds on
the same branch, set `timeout-minutes: 5` on jobs to prevent hung tasks, and use
`paths-ignore` under `push` and `pull_request` triggers to bypass CI for purely
non-functional/documentation changes.
