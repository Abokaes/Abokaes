## 2026-06-20 - Establishing Security Baseline in Minimal Repositories
**Vulnerability:** Lack of security disclosure policy and risk of accidental secret leakage via git.
**Learning:** Minimal repositories (like GitHub profile repos) often lack foundational security hygiene files, making them prone to accidental credential leakage if used for quick experiments or scripting.
**Prevention:** Always initialize repositories with a robust `.gitignore` covering common secrets (`.env`, `*.key`) and a `SECURITY.md` to redirect vulnerability reports from public issues to private channels.
