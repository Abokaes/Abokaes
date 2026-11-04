# Bolt Performance Journal

This journal records critical performance learnings and optimizations.

## 2026-11-03 - CI Workflow Concurrency and Path Filtering Optimization

**Learning:** Workflows without concurrency controls and path filters execute
redundant runner jobs during fast iterations and on documentation updates.
Using `cancel-in-progress: ${{ github.event_name == 'pull_request' }}` cancels
obsolete pull request runs without risking premature cancellation of main
branch deployments.
**Action:** Always configure concurrency groups with conditional cancellation
and ignore non-code paths in CI workflows.
