# Palette UX Journal

A repository of critical UX and accessibility learnings.

## 2026-07-24 - Accessible Emojis and Badge Horizontal Alignment

**Learning:** Screen readers struggle with raw emojis in text, reading them
without context or interrupting flow. Additionally, shields.io badges organized
vertically create significant clutter, and circular links degrade profile UX.

**Action:** Wrap all emojis in standard `<span role="img" aria-label="...">`
tags, organize shields.io badges horizontally using clean reference-style
links, and replace circular links with direct external contact points.
