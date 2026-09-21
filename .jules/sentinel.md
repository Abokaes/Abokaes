# Sentinel Security Journal

This journal records critical security learnings and hardening insights for this codebase.

## 2026-08-14 - CI Workflow Hardening

**Vulnerability:** Unpinned third-party GitHub Actions and unconstrained default runner permissions pose supply chain and privilege escalation risks.
**Learning:** Default GitHub Actions permissions can be overly permissive if repository defaults change, and mutable tag refs (like `@v4`) are susceptible to ref-poisoning attacks.
**Prevention:** Always declare explicit top-level `permissions: { contents: read }`, pin actions to full 40-character commit SHAs, and set explicit `timeout-minutes` on job runners.
