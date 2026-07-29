# Palette UX Journal

A specialized journal for tracking critical UX and accessibility learnings
discovered during the design and optimization of the user interfaces in this
repository.

## 2026-07-29 - Accessible GitHub Profile Layout and Navigation

**Learning:** GitHub profile READMEs act as modern visual resumes. Overuse of
emojis can overwhelm screen readers with redundant and disruptive auditory cues
unless they are wrapped in semantic spans with clear aria-labels. Furthermore,
vertical stacks of tech badges consume excessive vertical space, causing reader
fatigue. Grouping tech badges horizontally and offering skip navigation or
back-to-top links creates a highly scanable and responsive layout. Avoiding
redundant self-referencing links also ensures smooth screen reader navigation.

**Action:** Wrap every emoji (both decorative and structural) in a span tag
`<span role="img" aria-label="...">` to make it accessible. Lay out badge SVGs
horizontally, define links at the bottom, and provide clean local section links.
Keep lines under 80 characters.
