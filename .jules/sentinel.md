# Sentinel Security Journal

This journal records critical security learnings, findings, and architectural guidelines discovered during security assessments and hardening efforts.

## 2026-08-14 - Hardened GitHub Actions workflow permissions and checkout action

**Vulnerability:** Default GitHub Actions permissions were unconstrained and third-party action `actions/checkout` used a mutable tag (`@v4`).
**Learning:** Default GITHUB_TOKEN permissions can expose write access across repository resources if not limited explicitly at the workflow top level.
**Prevention:** Always declare `permissions: contents: read` at top level and pin third-party GitHub Actions to immutable full commit SHAs.
