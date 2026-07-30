# Palette UX Journal

This journal records critical user experience and accessibility learnings, specifically
focusing on accessibility compliance and design enhancements.

## 2026-07-29 - Structured and Accessible GitHub Profile READMEs

**Learning:** GitHub Profile READMEs often suffer from structural and
accessibility issues, such as missing top-level H1 headings, emojis lacking
screen reader context, long-running lines exceeding standard readability thresholds,
and vertical clutter from stacked non-horizontal badges. By introducing horizontal
layouts, semantic HTML element wraps for emojis, and explicit back-to-top
anchors, we can dramatically enhance screen reader accessibility and reading
flow.

**Action:** Wrap every emoji in a `<span role="img" aria-label="...">` tag, limit
line lengths strictly to 80 characters, use reference-style badge definitions at
the bottom to keep URLs and lines short, and include accessible, right-aligned
back-to-top link navigation to reduce scrolling fatigue.
