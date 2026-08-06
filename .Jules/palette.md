# Palette UX Journal

A journal dedicated to recording critical UX and accessibility learnings and
best practices.

## 2026-07-30 - Emoji Accessibility and Navigation in Profile READMEs

**Learning:** Wrapping emoji characters in inline HTML spans with role="img"
and aria-label ensures they are correctly interpreted by screen readers.
Additionally, inserting an HTML ID anchor inside the main H1 heading is a
powerful technique for creating functional, top-of-page scrolling navigation
links that do not violate markdownlint MD041 rules (first line must be a
top-level heading). Keeping all text lines strictly under 80 characters is
critical for readability and conforming to standard documentation formatting.

**Action:** Always wrap leading or decorative emojis in role="img" span
tags, and use inline ID anchors within the H1 heading for "Back to Top"
navigation anchors to maintain strict compliance with markdown lint rules and
maximize accessibility.
