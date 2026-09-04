# Palette UX Journal

This journal records critical UX and accessibility learnings discovered while
enhancing the user experience across the project.

## 2026-08-14 - Inline SVG Accessibility & Navigation Landmarks

**Learning:** SVG elements embedded in GitHub README profile pages lack
implicit screen reader roles and accessible labels, causing assistive
technologies to attempt reading child vector tags or lose visual context.
Additionally, long single-page profile layouts create scrolling fatigue without
top navigation anchors and proper heading hierarchy (MD001).

**Action:** Add explicit `role="img"` and `aria-label` to inline SVG graphics,
insert an inline anchor `<span id="top"></span>` into the main H1 heading, align
sub-heading increments (H1 -> H2), and provide right-aligned "Back to Top"
navigation links at major section boundaries.
