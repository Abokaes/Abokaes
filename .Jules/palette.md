# Palette UX Journal

This journal records critical UX and accessibility learnings from optimizing this
GitHub Profile.

## 2026-08-05 - Accessible Emojis and Anchors in GitHub Profiles

**Learning:** Screen readers often encounter issues with raw emojis and
confusing document structures when navigating GitHub Profile READMEs. Adding
proper semantic layout, wrapping all emojis in ARIA span elements, and providing
"Back to Top" navigation anchors inside the top-level H1 heading ensures a
seamless screen reader and keyboard-navigation experience.

**Action:** Wrap every emoji (including bullet-point leaders) in a span tag
`<span role="img" aria-label="...">` and use semantic HTML/Markdown reference
links to keep lines short and clean.
