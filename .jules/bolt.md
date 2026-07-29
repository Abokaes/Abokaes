# Bolt Performance Journal

This journal is maintained by Bolt ⚡ to record critical performance-related
learnings, insights, and anti-patterns encountered during repository and workflow
optimizations.

## 2026-07-28 - Optimizing GitHub Actions Workflow Execution

**Learning:** Unrestricted workflow triggers in basic repositories consume
unnecessary run time and concurrency limits. When a repository only contains
non-functional markdown documentation or configuration files, workflow runs
triggered by such changes are completely redundant.

**Action:** Implement `paths-ignore` for non-functional files and establish
strict concurrency control and job timeouts to significantly reduce compute
waste.
