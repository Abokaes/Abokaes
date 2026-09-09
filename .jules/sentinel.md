# Sentinel Security Journal

This journal records critical security learnings and vulnerability preventions
discovered during security hardening tasks in this repository.

## 2026-07-28 - Pinning GitHub Actions and Workflow Permissions

**Vulnerability:** Default permissive workflow execution and unpinned GitHub
Actions allow potential supply chain attacks or privilege escalation.

**Learning:** Unpinned third-party actions can be updated or hijacked if they
rely on moving tags like `@v4`. Default workflow permissions can write to code
by default.

**Prevention:** Always define explicit, write-restricted top-level permissions
(e.g., `contents: read`) and pin actions to full immutable commit SHAs.
