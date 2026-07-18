# Sentinel Security Journal

This security journal is used by Sentinel to record critical security-related
learnings and insights discovered during codebase analysis and hardening.

## 2026-07-17 - Workflow Hardening

**Vulnerability:** Excessive default permissions and unpinned third-party
Actions in CI workflows create risks of privilege escalation and supply chain
compromises.

**Learning:** GitHub Actions default to a broad set of token permissions (such
as write permissions for some scopes) if not explicitly restricted using the
`permissions` block, and mutable action tags can be dynamically updated.

**Prevention:** Always restrict workflows to `permissions: contents: read` as
the baseline default and pin third-party actions to immutable commit SHAs.
