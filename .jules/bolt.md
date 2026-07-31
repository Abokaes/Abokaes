# Bolt Performance Journal

This journal records critical performance learnings and optimizations implemented
for the repository.

## 2026-07-30 - CI Workflow Path Filtering and Concurrency

**Learning:** GitHub Actions workflows run on every push and pull request.
If the changes are only non-functional documentation or config files, running
the full CI build wastes CPU cycles, energy, and runner hours. Implementing
`paths-ignore` logic prevents redundant builds. Adding a `concurrency` block and
`timeout-minutes` controls execution duration and avoids wasting queue resources
on outdated commits.

**Action:** Add `paths-ignore` for `README.md`, `LICENSE`, and `.jules/**`. Add
a concurrency group, a `timeout-minutes: 5` limit, and pin actions to secure
SHAs.
