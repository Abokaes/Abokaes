## 2026-07-02 - GitHub Action Efficiency in Documentation Repos
**Learning:** In minimalist repositories like GitHub Profile READMEs, CI workflows often trigger on non-functional changes (README, LICENSE, metadata). This wastes runner minutes and delays feedback for actual code or workflow changes.
**Action:** Always implement `paths-ignore` for documentation and metadata files, and use `concurrency` with `cancel-in-progress: true` to optimize resource usage in these environments.
