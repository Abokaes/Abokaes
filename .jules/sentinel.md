# Sentinel Security Journal

This journal records critical security-related learnings, vulnerabilities,
fixes, and prevention strategies encountered during codebase hardening.

## 2026-07-28 - GitHub Actions Hardening

**Vulnerability:** Excessively permissive GitHub Actions workflow permissions,
lack of action pinning by commit SHA, and missing execution timeouts present high
security risks (e.g., token leakage, dependency hijacking, resource abuse).

**Learning:** CI workflows often run with default read/write permissions for the
GITHUB_TOKEN and refer to mutable tags (like @v4) which can be updated to point
to malicious code. Setting explicit minimal permissions and pinning to a specific
commit SHA is critical for preventing supply chain attacks.

**Prevention:** Always define explicit, minimal top-level permissions
(permissions: contents: read), pin third-party actions to verified commit SHAs,
and configure reasonable job execution timeouts (e.g., timeout-minutes: 5).
