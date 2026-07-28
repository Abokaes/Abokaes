# Palette UX Journal

A journal for recording critical UX and accessibility learnings in this
repository.

## 2026-07-28 - Enhancing Profile README Usability and Navigation

**Learning:** Profile pages act as professional landing zones. Unwrapped emojis
and vertical, text-only tech stacks increase vertical clutter and present
assistive technology barriers. Wrapping emojis in semantic container tags and
grouping technology badges horizontally in keyboard-navigable links dramatically
improves cognitive parsing and visual scanability. Adding localized section-skip
navigation controls avoids scroll fatigue.

**Action:** Wrap emojis in `<span role="img" aria-label="...">` tags, lay badges
out horizontally with direct external reference links, and include clear back-to-
top links for easy navigation. Keep line lengths within 80 characters.
