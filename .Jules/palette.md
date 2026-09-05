# Palette UX Journal

Critical UX and accessibility learnings captured by Palette 🎨.

## 2026-09-05 - Accessible SVG Graphics in GitHub Profile READMEs

**Learning:** Inline SVG graphics embedded in GitHub README profile pages require
explicit `role="img"`, `aria-label`, and `<title>` tags so assistive
technologies announce them as accessible visual elements rather than
attempting to read child vector tags.
**Action:** Always add `role="img"`, `aria-label="..."`, and a nested `<title>`
element to inline SVG elements in profile Markdown files.
