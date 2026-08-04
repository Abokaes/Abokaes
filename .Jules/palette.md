# Palette UX Journal

A journal dedicated to critical UX and accessibility learnings.

## 2026-08-03 - Accessible Profile Navigation & Imagery

**Learning:** When building GitHub profile READMEs, standard screen readers can
struggle with leading raw emojis in bulleted lists. Providing proper `aria-label`
wrappers and semantic `<span role="img">` tags is critical for unified visual
and screen reader experiences. In addition, avoiding circular links and
implementing reliable vertical scrolling "Back to Top" links with an inline
HTML anchor in the main H1 prevents scrolling fatigue for keyboard users.

**Action:** Wrap every emoji inside list items and headers in a standard accessible
span, set up `<span id="top"></span>` inside the H1 header, use reference-style
markdown links to avoid line length issues with badges, and provide clear
right-aligned anchor jumps.
