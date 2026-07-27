# Palette UX Journal

A journal for recording critical UX and accessibility learnings in this
repository.

## 2026-07-24 - Accessible Emojis and Visual Layout in Profile README

**Learning:** Unwrapped emojis in Markdown files can be highly disruptive or
unintelligible for screen reader users because different assistive technologies
lack standardized emoji support. Wrapping emojis in semantic `<span role="img"
aria-label="...">` tags ensures a consistent, friendly alternative description.
Furthermore, adding structured navigation lists and clean high-contrast
technology badges dramatically enhances accessibility and user experience in
GitHub Profile README documents.

**Action:** Wrap all emojis in standard `<span role="img" aria-label="...">`
elements. Implement clear jump-to targets with local anchor link index
sections, and always keep text line lengths under 80 characters.

## 2026-07-24 - Tech Badge Layout and Back-to-Top Navigation Links

**Learning:** Visual clutter and excessive vertical height in profile pages
can deter user engagement. Transitioning technology stack badges from a vertical
bullet list to a clean, single horizontal line reduces cognitive load and allows
immediate visibility. Additionally, adding keyboard-accessible "Back to Top"
navigation anchors at the end of long sections provides an intuitive way for
assistive tech and keyboard-only users to return to the global navigation
section without manual tedious scrolling.

**Action:** Organize technology and social badges horizontally where appropriate.
Insert responsive, clean right-aligned `<p align="right"><a
href="...">Back to Top</a></p>` links below major headings to optimize user navigation
flows.
