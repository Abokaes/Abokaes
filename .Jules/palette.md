# Palette UX Journal

This journal records critical UX and accessibility learnings for the Abokaes
profile project. Every entry must adhere to the 80-character line length limit
and begin with a top-level H1 heading.

## 2026-07-29 - Accessible GitHub Profile Layout

**Learning:** Accessible design in GitHub profile READMEs requires careful
handling of non-text elements (like emojis and badges) to prevent visual and
auditory fatigue. Screen readers can read emojis inline awkwardly, and vertical
clutter of tech badges degrades responsive reading. Wrapping emojis in
`span` elements with `role="img"` and `aria-label` provides a polished screen
reader experience. Grouping badges horizontally using bottom reference links
minimizes visual noise while adhering to the 80-character line length limit.

**Action:** For all future documentation and profiles, wrap every heading or
bullet emoji in `<span role="img" aria-label="...">` and define external badges
or links at the bottom of the document to keep the main text flow clean and
within readable character limits.
