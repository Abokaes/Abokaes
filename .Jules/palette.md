# Palette UX Journal

A journal of critical UX and accessibility learnings for the Abokaes profile
README.

## 2026-07-23 - Accessible Emojis in Markdown

**Learning:** Raw emojis in profile READMEs are not read accessibly by all
screen readers. Wrapping them in `<span role="img" aria-label="...">` is standard
practice. However, markdown linter rule MD033 (no-inline-html) restricts inline
HTML tags, so inline HTML needs to be selectively allowed or the lint rule
disabled.

**Action:** Wrap every emoji (including bullet icons) in standard span
wrappers and run markdownlint with MD033 disabled to ensure clean, valid
accessible Markdown.
