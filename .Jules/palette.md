# Palette UX Journal

Critical learnings regarding UX and accessibility in this repository.

## 2026-08-01 - Accessible Profile README Layouts

**Learning:** Standard GitHub profile templates often contain screen reader
unfriendly emojis, missing top-level H1 headings, and unpolished placeholders.
By using accessible inline HTML anchors for "Back to Top" navigation,
structuring badges as bottom-of-file references, and wrapping all emojis in
role-labeled span tags, we significantly improve screen reader compatibility and
prevent scrolling fatigue.
**Action:** Always wrap emojis in `<span role="img" aria-label="...">` and define
shields.io badges as references at the bottom of the file to adhere to line
length limits.
