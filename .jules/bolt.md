## 2025-05-14 - Optimizing Minimalist CI Workflows
**Learning:** In repositories with minimal codebases (like GitHub Profile READMEs), CI overhead often exceeds execution time. Strategic use of `concurrency` (canceling redundant runs) and `fetch-depth: 1` (shallow clones) can significantly reduce resource waste and wait times, even if the "build" itself is fast.
**Action:** Always check for `concurrency` and `fetch-depth` optimizations in GitHub Actions, especially for documentation-heavy or minimalist repositories.
