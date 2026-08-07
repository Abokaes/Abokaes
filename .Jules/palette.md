# Palette UX Journal

A journal to record critical UX and accessibility learnings from optimizing
interfaces and user experiences.

## 2026-08-07 - Profile README Accessibility and Usability Refinement

**Learning:** Creating a welcoming and accessible GitHub profile README requires
proper semantic header structure (MD041/first-line-h1), strict screen reader
support for emojis, and a cohesive horizontal visual layout that respects standard
80-character line constraints (MD013). Including "Back to Top" anchors helps users
navigate longer profiles seamlessly without scrolling fatigue.
**Action:** Always start README files with an H1 heading featuring an inline HTML
anchor `<span id="top"></span>`. Wrap emojis in spans with `role="img"` and
`aria-label`. Use horizontal tech stack layouts with reference-style Markdown
links to prevent long lines, and add navigation helper links at the end of sections.
