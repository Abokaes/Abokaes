# Sentinel Security Journal

This journal records critical security learnings, findings, and best practices discovered while securing the codebase.

## 2026-08-14 - Hardening GitHub Actions CI Workflows
**Vulnerability:** GitHub Actions workflows running with default broad `GITHUB_TOKEN` permissions and unpinned action tags (`actions/checkout@v4`) can be vulnerable to token abuse and upstream supply chain tampering.
**Learning:** In unconfigured workflows, `GITHUB_TOKEN` defaults to read-write scope on repository contents. Furthermore, floating action tags (like `@v4`) are mutable tags that can be updated upstream to point to malicious code.
**Prevention:** Always declare strict top-level `permissions` (e.g. `contents: read`), pin third-party actions to full commit SHAs, and add explicit `timeout-minutes` to avoid denial-of-service/resource exhaustion.
