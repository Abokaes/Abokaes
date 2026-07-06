## 2026-07-02 - CI Efficiency via Path Ignoring
**Learning:** In minimalist repositories like GitHub Profile READMEs, the majority of updates are non-functional (README edits, journal entries). Triggering CI for these changes wastes GitHub Actions runner minutes.
**Action:** Always implement `paths-ignore` for non-functional files and use `timeout-minutes` to guard against hung processes in these environments.
