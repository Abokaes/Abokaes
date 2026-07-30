# Sentinel Security Journal

This journal records critical security learnings and vulnerability patterns
discovered and fixed in the repository.

## 2026-07-29 - GitHub Actions Workflow Hardening

**Vulnerability:** Excessively permissive GitHub Actions workflow permissions, lack
of step execution timeouts, and dependency on mutable action tags (like @v4).
Permissive default GITHUB_TOKEN permissions could allow compromised workflows to
modify repository contents or settings. Mutable tags could lead to supply chain
attacks if the tag is pointed to a malicious commit.

**Learning:** GitHub Actions defaults are historically permissive. Workflows must
explicitly restrict `permissions` to `contents: read` (or the minimum required)
at the top level to adhere to the principle of least privilege. In addition,
pinning actions to their full immutable commit SHAs protects against tag
spoofing and compromised action code. Setting timeouts prevents hung tasks
from consuming execution minutes.

**Prevention:** Always define explicit top-level permissions in workflow files,
pin all external actions to a cryptographically secure commit SHA rather than
using tags, and define timeout configurations for all jobs or steps.
