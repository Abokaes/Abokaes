# Palette UX Journal

A record of critical UX/accessibility learnings discovered while enhancing the
interfaces in this repository.

## 2026-07-29 - Screen Reader Accessible Emojis

**Learning:** Emojis are frequently read incorrectly or can disrupt screen
readers if not properly annotated. Wrapping emojis in semantic `span` tags with
`role="img"` and an appropriate `aria-label` provides a consistent and
accessible auditory experience for visually impaired users.

**Action:** Wrap all emojis in `<span role="img" aria-label="...">` tags to
guarantee standard screen-reader support.
