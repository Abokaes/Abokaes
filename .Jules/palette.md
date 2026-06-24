## 2025-05-14 - Balancing Accessibility and Markdown Readability

**Learning:** While wrapping emojis in `<span role="img" aria-label="...">` tags adheres to high accessibility standards, it can significantly degrade the source readability of Markdown files. Over-applying this pattern, especially in commented-out template blocks, is perceived as "noisy" and maintenance-heavy by reviewers.

**Action:** Prioritize applying accessibility enhancements to user-visible elements only. When working with Markdown, weigh the benefit of custom ARIA labels against the readability of the raw file and the capabilities of modern screen readers.
