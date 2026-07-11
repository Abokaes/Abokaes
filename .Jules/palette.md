# Palette's Journal

This journal records critical UX and accessibility learnings discovered during the development of this project.

## 2026-07-07 - Structural Accessibility in Profile READMEs

**Learning:** For proper structural accessibility in GitHub Profile READMEs, the document must start with a top-level H1 heading (#) to establish the correct hierarchy for screen readers. Additionally, wrapping emojis in semantic spans with ARIA labels ensures they are properly announced, and keeping line lengths within 80 characters optimizes readability for all users.

**Action:** Always verify README structure with `markdownlint-cli` and ensure emojis are accessible and lines are wrapped.
