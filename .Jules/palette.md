# Palette UX Journal

A journal to record critical UX and accessibility learnings from optimizing
interfaces and user experiences.

## 2026-08-09 - Accessibility and Readability Standards in Profile READMEs

**Learning:** Profile READMEs are highly visual entryways. Unwrapped emojis can
confuse screen readers, and unstructured tech badge listings decrease horizontal
scannability. Wrapping emojis in semantic tags, laying tech badges out
horizontally under strict 80-character line limit, and providing clear "Back to
Top" navigation controls significantly improves usability and accessibility.

**Action:** Wrap all emojis with `<span role="img" aria-label="...">`, align
badges horizontally using short referenced links, limit line lengths to 80
characters, and place top-scrolling anchors on the main heading.
