# Palette UX Journal

This journal records critical UX and accessibility learnings from working on
the Abokaes/Abokaes GitHub Profile README user interface.

## 2026-07-30 - Standardizing Accessible Navigational Structures in Profile READMEs

**Learning:** GitHub Profile READMEs serve as a personal developer hub, but can
suffer from scroll fatigue and visual clutter if the content is long and unguided.
Wrapping interactive emojis in `<span role="img" aria-label="...">` ensures
semantic screen reader support. Placing an HTML target id inside the top H1
heading (like `<span id="top"></span>`) allows users to navigate back to the
beginning using well-placed, accessible, right-aligned anchor links. Grouping
badges horizontally prevents vertical line sprawl and makes the page extremely
scannable for both screen readers and visual users.

**Action:** In all profile-level documentations, integrate structured sections
featuring accessible emoji spans, horizontal badge arrangements to reduce clutter,
and convenient "Back to top" links tied to a top-heading anchor target. Always
keep lines under 80 characters to adhere to readability best practices.
