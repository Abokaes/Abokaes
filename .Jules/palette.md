## 2025-05-14 - Accessible Emoji Links in Markdown
**Learning:** In GitHub Profile READMEs, using emojis as bullet points or within link text is common but often inaccessible. Wrapping them in `<span role="img" aria-label="...">` ensures screen readers can describe the visual context provided by the emoji.
**Action:** Always wrap emojis in profile READMEs with appropriate ARIA roles and labels, especially when they precede links or serve as headers.
