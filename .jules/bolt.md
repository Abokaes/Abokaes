## 2025-05-15 - Optimizing CI/CD Efficiency in Minimal Repositories
**Learning:** Even in repositories that primarily serve as profiles or documentation (like GitHub Profile READMEs), the CI/CD pipeline (GitHub Actions) can be a source of inefficiency. Missing `concurrency` controls and `paths-ignore` for non-code files lead to redundant runs and wasted compute resources.
**Action:** Always audit GitHub Actions for infrastructure-level performance wins: implement `concurrency` to cancel outdated builds and `paths-ignore` to skip runs for documentation-only updates.
