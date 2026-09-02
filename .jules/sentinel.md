# Sentinel Security Journal

This journal tracks critical security learnings, vulnerability patterns, and security hardening measures across the project.

## 2026-08-07 - Repository Security Baseline & Hardened Workflows

**Vulnerability:** Unpinned third-party GitHub Actions, missing explicit token permissions (`permissions`), missing timeout limits, and absent baseline security files (`.gitignore`, `SECURITY.md`).
**Learning:** Default GitHub Actions configurations grant broad `GITHUB_TOKEN` permissions and unpinned actions can introduce supply chain risks if compromised upstream.
**Prevention:** Always declare explicit read-only permissions (`permissions: contents: read`), pin actions to explicit 40-character commit SHAs, set execution timeouts, and maintain explicit `.gitignore` and `SECURITY.md` files.
