# Palette UX Journal

A journal dedicated to critical UX and accessibility learnings from optimizing
interfaces, with a primary focus on the GitHub profile README and accessibility.

## 2026-07-24 - Accessible Emojis and Structured Navigation

**Learning:** Emojis are widely used in modern layouts but can degrade screen
reader experience if not wrapped in custom tags with semantic ARIA attributes.
Additionally, using circular references (like links pointing back to the current
user profile) hurts the navigation flow; externalizing references to specific
repository components or tools provides a much more intuitive journey.

**Action:** Wrap all emojis in `<span role="img" aria-label="...">` and replace
redundant profile references with direct mailto, repository, or issue URLs.
