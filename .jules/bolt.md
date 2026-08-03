# Bolt Performance Journal

This journal is maintained by Bolt ⚡, a performance-obsessed agent, to
record critical performance-related learnings. Every entry captures
codebase-specific performance patterns, bottlenecks, and optimization
surprises to avoid future mistakes.

## 2026-08-01 - Optimized GitHub Actions CI Workflow

**Learning:** GitHub Actions workflows can waste runner minutes and billing costs
by triggering unnecessary runs on non-code changes (such as README.md or
journal updates) or running multiple workflows for consecutive pushes. Adding
concurrency controls, paths-ignore filters, and job-level timeouts optimizes
resource utilization and prevents infinite billing waste.

**Action:** Always implement a top-level `concurrency` block, add filter logic
like `paths-ignore` for documentation and markdown files, specify explicit
workflow timeouts, and secure workflow permissions via `permissions:
contents: read`.
