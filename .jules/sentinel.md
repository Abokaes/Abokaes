## 2026-07-02 - GitHub Actions Hardening
**Vulnerability:** CI workflows using default (potentially permissive) permissions, lacking timeouts, and using mutable tags for actions.
**Learning:** Default GitHub Action configurations can be overly permissive and vulnerable to supply chain attacks if tags are compromised.
**Prevention:** Always set explicit top-level `permissions`, define job `timeout-minutes`, and pin actions to specific SHAs.
