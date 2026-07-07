## 2026-07-07 - GitHub Actions Hardening
**Vulnerability:** Default GHA workflows often have overly broad permissions and lack resource constraints or supply chain protections.
**Learning:** Pinning actions to SHAs and setting explicit minimal permissions significantly reduces the attack surface of the CI/CD pipeline.
**Prevention:** Always set top-level permissions, job-level timeouts, and pin actions to specific commit hashes.
