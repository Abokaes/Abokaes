## 2026-07-02 - GitHub Actions Hardening
**Vulnerability:** Default GITHUB_TOKEN permissions are overly permissive (read/write), lack of job timeouts can lead to resource exhaustion, and action tags can be mutated (supply chain risk).
**Learning:** Even a "blank" or basic workflow should be hardened by default to follow the principle of least privilege and protect the supply chain.
**Prevention:** Always set `permissions: contents: read` at the top level, pin actions to a full 40-character SHA, and set `timeout-minutes` for all jobs.
