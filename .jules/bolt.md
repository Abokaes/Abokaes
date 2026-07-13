# Bolt Performance Journal

This journal is for recording critical performance-related learnings.

## 2026-07-13 - Optimizing CI for Minimalist Repositories
**Learning:** In repositories where the primary content is documentation (like a GitHub Profile README), CI runs on every push to files like `README.md` or `LICENSE` are unnecessary and consume runner minutes without providing value.
**Action:** Always implement `paths-ignore` for non-functional files and add `timeout-minutes` to jobs to prevent resource waste and ensure fast failure in case of hangs.
