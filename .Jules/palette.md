# Palette UX Journal

A journal dedicated to critical UX and accessibility learnings for
Abokaes/Abokaes.

## 2026-08-06 - Profile README Micro-UX and Accessibility Hardening

**Learning:** Organizing technology badges horizontally rather than vertically
reduces visual clutter and prevents cognitive overload when loading a user
profile. Additionally, adding functional right-aligned "Back to Top" links
using an inline HTML anchor inside the top-level H1 prevents scrolling fatigue
on longer profiles without violating MD041 markdownlint constraints.

**Action:** Always place `<span id="top"></span>` inside the top-level H1
heading to support keyboard and scroll navigation, and map external reference
links at the bottom of the document to keep the text body concise and readable.
