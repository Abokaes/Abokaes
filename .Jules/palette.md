# Palette UX Journal

## 2026-07-16 - Accessible Profile README Emojis and Links

**Learning:** When documentation (like a GitHub Profile README) acts as the
primary user interface, UX is driven by readability and semantic structure.
Unlabeled emojis can confuse screen readers, while circular links create
repetitive navigation loops.

**Action:** Wrap every emoji (including bullet icons and headers) in custom
accessible `<span role="img" aria-label="...">` tags for screen readers,
enforce an 80-character limit, and replace self-referential profile links with
direct, actionable resources such as repository issue paths.
