# Palette UX Journal

## 2026-07-17 - Profile README Accessibility Improvement

**Learning:** GitHub Profile READMEs serve as a primary user interface for
developers, and wrapping profile emojis in accessible span tags ensures screen
readers provide a polite, uniform, and semantic reading experience. Circular
references (e.g. links pointing back to the profile itself) create confusing
UX loops and should be replaced with direct external actions like issue
creation.

**Action:** Always verify profile links to ensure they point to constructive,
direct external paths, use accessible html span elements with aria-label for
emojis, and keep line lengths below 80 characters to satisfy documentation
accessibility standards.
