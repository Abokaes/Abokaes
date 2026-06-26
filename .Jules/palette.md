# Palette's Journal

## 2026-06-26 - Accessibility and Hygiene in Profile READMEs
**Learning:** GitHub's Markdown renderer strips `role` and `aria-label` attributes from `<span>` tags, making emoji accessibility labels technically ineffective in the final rendered profile. However, maintaining these labels in the source code is a project standard. Additionally, using temporary HTML files for Playwright verification requires strict cleanup to avoid polluting the repository.
**Action:** Continue implementing ARIA labels for emojis for source-level accessibility, and ensure all verification artifacts (like .html files) are removed before PR submission.
