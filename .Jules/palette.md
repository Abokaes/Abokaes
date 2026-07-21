# Palette UX Journal

Critical UX and accessibility learnings from designing user interfaces.

## 2026-07-17 - Accessible Emojis in Profile templates

**Learning:** Emojis in list-items or text can cause screen readers to
interrupt flow or misinterpret icons. For consistent accessibility, they
should be wrapped in `<span role="img" aria-label="...">` tags.
**Action:** Always wrap all inline and list-item emojis in semantic span
elements with correct ARIA labels.
