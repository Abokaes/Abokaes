## 2025-06-24 - Do not ignore pnpm-lock.yaml in security baseline
**Vulnerability:** Inconsistent dependency resolution across environments if lockfiles are ignored.
**Learning:** Initially included `pnpm-lock.yaml` in `.gitignore` thinking of it as a generated file, but lockfiles are critical for security to ensure the same dependency tree is used in CI and production, preventing supply chain attacks.
**Prevention:** Always track lockfiles (`pnpm-lock.yaml`, `package-lock.json`, etc.) in the repository to ensure reproducible and secure builds.
