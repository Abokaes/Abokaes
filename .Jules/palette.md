# Palette UX Journal

This journal records critical UX/accessibility learnings discovered during
the development and enhancement of the user interface.

## 2026-07-17 - Accessible Markdown and Structural Headers

**Learning:** Standard Markdown files used as profile READMEs or documentation
frequently contain accessibility gaps, such as missing top-level structural
headings, un-wrapped emoji characters that screen readers parse without
context, and poorly formatted text layouts. Ensuring files strictly start with
a top-level H1 header improves document outline navigation for screen readers.
Wrapping emoji characters in `<span role="img" aria-label="...">` ensures that
screen readers can explicitly read the emoji's meaning to the user rather than
relying on default text-to-speech interpretations.

**Action:** Always start Markdown files with a single H1 header. Restrict all
lines to 80 characters or fewer for improved visual parsing and reading comfort.
Wrap all presentational or informational emojis in standard, accessible span
elements with correct role and aria-label attributes.
