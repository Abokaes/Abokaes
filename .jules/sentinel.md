# Sentinel Security Journal

This security journal is used by Sentinel to record critical security-related
learnings and insights discovered during codebase analysis and hardening.

## 2026-11-09 - Workflow Hardening

**Vulnerability:** Excessive default permissions, unpinned third-party
actions, and missing execution timeouts in CI workflows create risks of token
privilege escalation, supply chain compromise, and Denial of Service.

**Learning:** GitHub Actions workflows default to broad token permissions if
not explicitly restricted with `permissions: contents: read`. Mutable action tags
can be maliciously modified or hijacked, making immutable commit SHA pinning
essential.

**Prevention:** Always declare explicit minimal permissions at the workflow
level, pin third-party actions to full commit SHAs, and specify job execution
timeouts.
