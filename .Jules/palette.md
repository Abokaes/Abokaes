# Palette UX Journal

This journal records critical UX and accessibility learnings from working on
the Abokaes/Abokaes GitHub Profile README user interface.

## 2026-07-17 - Accessible Emojis in GitHub Profile Markdown

**Learning:** Wrapping emojis in HTML `<span role="img" aria-label="...">` tags
significantly improves screen reader accessibility, ensuring assistive
technologies speak the proper semantic description of the emojis rather than
ignoring or mispronouncing them. However, since `markdownlint` flags raw HTML
using rule MD033 (no-inline-html), this rule must be selectively disabled when
linting files that prioritize these accessible patterns.
**Action:** When designing Markdown interfaces with assistive technology in
mind, consistently wrap every emoji in semantic spans and configure linting to
ignore MD033 on those files to prevent false-positive build/lint failures.
