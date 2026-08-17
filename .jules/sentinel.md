# Sentinel Security Journal

This journal records critical security-related learnings, patterns, and constraints discovered while securing the repository.

## 2026-08-07 - Repository Security Baseline
**Vulnerability:** Initial security audit revealed default workflow missing explicit permissions, unpinned action dependencies, and no job timeout limits.
**Learning:** Default GitHub Actions templates lack security best practices such as least-privilege permissions and SHA action pinning.
**Prevention:** Always declare top-level `permissions: contents: read`, set job timeouts, and pin action dependencies to exact commit SHAs.
