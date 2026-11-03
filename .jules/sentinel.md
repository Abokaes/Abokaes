# Sentinel Security Journal

Security learnings and decisions for the repository.

## 2026-11-02 - GitHub Actions Workflow Hardening
**Vulnerability:** Default CI workflows lack explicit permissions, run with mutable third-party action tags, and lack job execution timeouts, exposing runners to privilege escalation, supply chain action compromise, and denial-of-service/resource exhaustion.
**Learning:** GitHub Actions defaults to permissive repository permissions unless explicitly restricted, and mutable action tags like `@v4` can be hijacked or retargeted if upstream accounts are compromised.
**Prevention:** Enforce top-level read-only permissions (`permissions: contents: read`), pin all third-party actions to immutable commit SHAs, and set defensive job execution timeouts (`timeout-minutes`).
