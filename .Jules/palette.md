## 2025-05-14 - Accessible Emojis and Quick Links in Profile README

**Learning:** GitHub's Markdown renderer supports HTML tags like `<span>`, which can be used to wrap emojis with `role="img"` and `aria-label` to provide context to screen reader users who might otherwise hear only the emoji's default description. Additionally, a "Quick Links" section in a profile README provides immediate functional value by reducing the clicks needed to reach common user activity tabs.

**Action:** Always wrap informative or decorative emojis in `<span role="img" aria-label="...">` when used in Markdown to ensure accessibility. Include a "Quick Links" section in profile READMEs to improve navigation UX.
