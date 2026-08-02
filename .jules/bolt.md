# Bolt Performance Journal

This journal records critical performance learnings and optimizations.

## 2026-08-01 - Optimize CI workflow execution

**Learning:** CI build pipelines can consume unnecessary runner minutes
by executing builds on non-functional or documentation updates (like README).
They also waste resources if duplicate workflow runs are not canceled.

**Action:** Implement paths-ignore for markdown, license, and journal files, and
use concurrency groups with cancel-in-progress: true to terminate duplicate/stale
runs automatically.
