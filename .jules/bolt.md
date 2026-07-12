# Bolt Performance Journal

## 2026-07-07 - CI/CD Workflow Optimization
**Learning:** In minimalist repositories where the primary content is a README, GitHub Actions workflows can be triggered unnecessarily by non-functional changes (documentation, configuration, license). Using `paths-ignore` significantly reduces redundant runner usage.
**Action:** Always include `paths-ignore` for non-functional files like `README.md`, `LICENSE`, and agent-specific directories in GitHub Action triggers.
