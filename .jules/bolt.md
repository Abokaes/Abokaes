# Bolt Performance Journal

This journal records critical performance-related learnings from optimizing
workflows, architectures, and other systems.

## 2026-08-09 - GitHub Actions CI Efficiency Optimization

**Learning:** Standard GitHub Actions configurations run on every commit or PR
by default. In repositories primarily used for GitHub Profile READMEs, running
a full build job on documentation edits or redundant commits wastes precious CI
runner minutes. Adding paths-ignore prevents non-functional files from triggering
runs, while setting concurrency groups automatically cancels older runs when new
commits are pushed.

**Action:** Add `paths-ignore` for documentation and metadata files, configure a
concurrency group with `cancel-in-progress: true`, and specify strict job-level
timeouts to prevent runaway builds from consuming billing minutes.
