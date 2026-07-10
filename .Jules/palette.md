# Palette Journal

## 2026-07-07 - Emoji Accessibility in Markdown

**Learning:** Emojis in Markdown are often read by screen readers as their raw
character code or a generic description. Wrapping them in HTML span tags with
role="img" and an aria-label provides a consistent and meaningful experience
for assistive technology users.

**Action:** Always wrap emojis in <span role="img" aria-label="..."> when used
in documentation files like README.md.
