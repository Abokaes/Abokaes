# Bolt Performance Journal

This journal records critical performance-related learnings.

## 2026-08-01 - CI Workflow Concurrency and Path Filtering

**Learning:** Optimizing GitHub Actions workflows using top-level concurrency
(cancel-in-progress) and path-ignore filtering prevents redundant jobs and
unnecessary run queue blocks.

**Action:** Implement concurrency blocks and exclude markdown/metadata files
from triggering CI jobs in blank.yml.
