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

## 2026-07-24 - Navigation Index and Tech Badges in Profile README

**Learning:** Navigating long documentation or profile screens can be tedious
and inaccessible for keyboard and screen-reader users without clear jump-to
targets. Adding a dedicated "Quick Navigation" section with local link anchors
greatly enhances readability and navigation speed. Additionally, providing
high-contrast technology badges improves aesthetic polish, but they must use
descriptive alt tags instead of generic placeholders to remain fully accessible
to screen-reader users.

**Action:** Always include a Quick Navigation section for profile readmes or
longer documentation. Use high-contrast badges to visually list technologies,
and ensure they include descriptive alt tags, wrapping all emojis in standard
accessible spans. Keep line lengths under 80 characters.
