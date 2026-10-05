# Sentinel Security Journal

This journal records critical security-related learnings, vulnerabilities,
fixes, and prevention strategies encountered during codebase hardening.

## 2026-08-14 - GitHub Actions Hardening

**Vulnerability:** Excessively permissive default GitHub Actions permissions,
unpinned third-party actions using mutable tags, and lack of execution timeouts.

**Learning:** Unpinned actions can be compromised upstream leading to supply-chain
attacks, while unrestricted GITHUB_TOKEN permissions increase exposure if a job is
compromised.

**Prevention:** Explicitly restrict GITHUB_TOKEN permissions to `contents: read`,
pin third-party actions to full commit SHAs, and set reasonable `timeout-minutes`.
