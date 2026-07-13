# Palette UX Journal

This journal tracks critical UX and accessibility learnings from working on this repository.

## 2026-07-12 - Accessible Emoji Patterns in Markdown

**Learning:** Emojis used in Markdown headers are often ignored or
misinterpreted by screen readers. Wrapping them in a semantic HTML span with
`role="img"` and a descriptive `aria-label` ensures that the decorative or
informative nature of the emoji is properly communicated to all users without
breaking the visual layout.

**Action:** Always wrap decorative or informative emojis in GitHub READMEs with
`<span role="img" aria-label="...">...</span>` and ensure `markdownlint` is
configured to allow inline HTML (MD033) for these specific spans.
