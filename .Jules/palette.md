# Palette UX Journal

## 2026-07-17 - Accessible Emoji Integration in Profile READMEs

**Learning:** When building minimalist or profile-focused user interfaces (such
as a GitHub Profile README), using bare emojis can cause screen reader issues or
feel unpolished. Emojis must be wrapped in `<span role="img"
aria-label="...">` tags to provide clear alternative text. Furthermore, line
lengths in markdown should be kept strictly under 80 characters to enhance
readability and prevent horizontal scrolling.

**Action:** Wrap every emoji in a descriptive span element and format markdown
text to have lines of 80 characters or fewer.
