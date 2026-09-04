# Palette UX Journal

Critical UX and accessibility learnings from repository interactions.

## 2026-08-09 - Accessible Interactive Disclosure Pattern
**Learning:** Collapsible sections using native HTML `<details>` and
`<summary>` provide clean, keyboard-accessible UI interaction in GitHub GFM
without relying on JavaScript.
**Action:** Use native HTML disclosure elements for supplementary content on
long profile pages.

## 2026-08-14 - Accessible Back to Top Navigation Links
**Learning:** Adding right-aligned 'Back to Top' anchor links below major
sections of long Profile READMEs prevents user scrolling fatigue and improves
keyboard/screen reader navigation.
**Action:** Include `<span id="top"></span>` in top-level headings and place
`href="#top"` anchors under major sections.
