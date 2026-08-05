# Palette UX Journal

This journal records critical UX and accessibility learnings for the Abokaes
repository.

## 2026-08-05 - Accessible Emoji Patterns and Navigation Anchors

**Learning:** When using emojis in lists, wrapping them in `<span role="img"
aria-label="...">` ensures screen readers read them correctly. Furthermore,
providing a `<span id="top"></span>` inside the main H1 heading is an elegant
way to implement back-to-top navigation without violating MD041 markdownlint
rules.

**Action:** Wrap emojis in spans with descriptive role/aria-label attributes
and place the top-level anchor inside the H1 tag. Keep lines under 80 chars.
