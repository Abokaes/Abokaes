## 2026-06-21 - CI Efficiency in Minimal Repositories
**Learning:** Even in repositories without source code (like GitHub Profile READMEs), CI workflows can be inefficient by running on every metadata change or lacking resource limits.
**Action:** Always implement `paths-ignore` for documentation-only changes and set `concurrency` and `timeout-minutes` to save runner resources.
