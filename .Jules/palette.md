## 2025-05-14 - Accessible Emojis in Markdown
**Learning:** Screen readers often announce emojis inconsistently or skip them. Wrapping them in `<span role="img" aria-label="...">` ensures that the intended meaning is conveyed to all users, especially when used as visual cues for headers.
**Action:** Always wrap emojis in ARIA-compatible tags when modifying Markdown files in this repository.
