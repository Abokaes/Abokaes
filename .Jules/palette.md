# Palette's Journal

## 2026-03-06 - [Emoji Accessibility in README]
**Learning:** Emojis in a project's README (which serves as the primary landing page on GitHub) should be wrapped in semantic HTML with ARIA labels to ensure they are accessible to screen reader users.
**Action:** Always wrap emojis in `<span role="img" aria-label="...">` when they convey meaning or greeting in a UI context, including README files.
