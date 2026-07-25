# Palette UX Journal

A journal for recording critical UX and accessibility learnings in this
repository.

## 2026-07-24 - Accessible Emojis in Markdown

**Learning:** Unwrapped emojis in Markdown files can be confusing or disruptive
for screen reader users, as standard screen readers might read them out of
context or fail to describe them correctly. Wrapping emojis in semantic HTML
`span` elements with `role="img"` and `aria-label="..."` provides a clean,
accessible alternative text that makes the document highly readable for screen
readers.

**Action:** Wrap all emojis in standard Markdown files (such as README.md and
project documentation) in `<span role="img" aria-label="...">` tags. Disable
the MD033 (no-inline-html) lint rule in markdownlint-cli specifically to permit
these tags while keeping other structural lint rules intact.
