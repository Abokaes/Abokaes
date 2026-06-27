## 2025-05-15 - Markdown Link Parser Sensitivity
**Learning:** Some Markdown parsers (like `markdown-it`) fail to render `<a>` tags if the URL in a `mailto:` link contains bracketed placeholders (e.g., `(mailto:[email])`). This results in the raw Markdown string being displayed instead of a clickable link.
**Action:** Use plain text or standard email formats for placeholders within `mailto:` links to ensure consistent rendering across different Markdown engines.
