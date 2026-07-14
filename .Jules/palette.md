# Palette UX Journal
This journal is reserved for critical UX and accessibility learnings identified during the development of this repository.

## 2026-07-12 - Accessible Emojis in Markdown
**Learning:** Emojis used as decorators or list bullets in Markdown are not accessible by default to screen readers. Wrapping them in `<span role="img" aria-label="...">` tags provides the necessary semantic context.
**Action:** Always wrap emojis in accessible spans when they convey meaning or serve as visual cues in documentation-centric interfaces.
